<template>
  <q-page class="q-ma-md">
    <h3>FormsPage</h3>
    <q-separator spaced />

    <div class="row justify-center">
      <q-form
        @submit="onSubmit"
        @reset="onReset"
        class="q-gutter-xs col-xs-12 col-sm-12 col-md-6 q-pt-xl"
      >
        <q-input
          filled
          v-model="userForm.email"
          label="Correo Electronico"
          type="email"
          lazy-rules
          :rules="[
            (val) => (val && val.length > 0) || 'Campo Obligatorio',
            (val) => isValidEmail(val),
          ]"
        />
        <q-input
          filled
          type="password"
          v-model="userForm.password1"
          label="Password"
          lazy-rules
          :rules="[
            (val) => (val !== null && val !== '') || 'Contrasena obligatoria',
          ]"
        />

        <q-input
          filled
          type="password"
          v-model="userForm.password2"
          label=" Confirmar Password"
          lazy-rules
          :rules="[
            (val) => (val !== null && val !== '') || 'Contrasena obligatoria',
            (val) => isSamePss(val),
          ]"
        />
        <q-checkbox
          v-model="userForm.conditions"
          label="Aceptar condiciones"
          :style="
            userForm.errorInconditions && !userForm.conditions && 'color:red'
          "
        />

        <div class="row justify-end">
          <q-btn
            label="Reset"
            type="reset"
            color="primary"
            flat
            class="q-ml-sm"
          />
          <q-btn label="Submit" type="submit" color="primary" />
        </div>
      </q-form>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import { useQuasar } from "quasar";

export default defineComponent({
  name: "FormsPage",
  setup() {
    const $q = useQuasar();

    const userForm = ref({
      email: "",
      password1: "",
      password2: "",
      conditions: false,
      errorInconditions: false,
    });

    return {
      userForm,

      onSubmit() {
        userForm.value.errorInconditions = false;
        if (!userForm.value.conditions) {
          $q.notify({
            message: "acepte las condiciones y terminos para continuar",
            icon: "las la-exclamation-circle",
          });
          userForm.value.errorInconditions = true;
          return;
        }
      },
      onReset() {
        userForm.value.modelValue = {
          email: "",
          password1: "",
          password2: "",
          conditions: false,
          errorInconditions: false,
        };
      },
      isValidEmail(val) {
        const emailPattern =
          /^(?=[a-zA-Z0-9@._%+-]{6,254}$)[a-zA-Z0-9._%+-]{1,64}@(?:[a-zA-Z0-9-]{1,63}\.){1,8}[a-zA-Z]{2,63}$/;
        return emailPattern.test(val) || "El correo no parece ser válido";
      },
      isSamePss(val) {
        return val === userForm.value.password1 || "contrasenas no coinciden";
      },
    };
  },
});
</script>

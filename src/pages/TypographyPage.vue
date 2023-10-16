<template>
  <q-page class="flex column q-pa-md">
    <span class="text-h1"> Typography </span>
    <span class="text-h2"> Typography </span>
    <span class="text-h3"> Typography </span>
    <span class="text-h4"> Typography </span>
    <span class="text-h5"> Typography </span>
    <q-separator />
    <span class="text-subtitle1"> subtitle 1 </span>
    <span class="text-subtitle2"> subtitle 2 </span>
    <q-separator />
    <p class="text-body1">
      Incididunt ex laboris adipisicing culpa anim ea est amet et pariatur ea
      Lorem dolor dolor. Dolor deserunt mollit elit ad duis laboris exercitation
      voluptate. Enim dolor culpa enim ad non nisi dolor ea qui. Sunt eiusmod
      proident in consequat duis esse ad labore elit. Ut excepteur incididunt
      qui excepteur consectetur ad laboris adipisicing fugiat ipsum Lorem. Sint
      non nostrud enim anim pariatur nostrud culpa est deserunt culpa
      adipisicing. Irure tempor tempor excepteur ut sit culpa voluptate proident
      sit commodo do dolor proident qui.
    </p>
    <p class="text-body2">
      Voluptate non minim incididunt mollit culpa dolore labore in do laboris.
      Qui esse magna tempor ut reprehenderit veniam reprehenderit laborum anim
      aliqua aute dolore. Ipsum fugiat in officia adipisicing est do. Deserunt
      laboris labore dolor ea ea aliqua pariatur cillum excepteur. Nulla
      proident enim excepteur cupidatat anim enim minim quis deserunt minim
      consectetur ipsum.
    </p>
    <q-btn
      color="primary"
      :label="sideMenuOpen ? 'Cerrar Menu lateral' : 'Abrir Menu lateral'"
      class="q-mt-md"
      @click="toggleSideMenu"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import useUI from "src/composables/useUI";

export default defineComponent({
  name: "TypographyPage",

  setup() {
    const { sideMenuOpen, toggleSideMenu } = useUI();

    return {
      sideMenuOpen,
      toggleSideMenu,
    };
  },
});
</script>

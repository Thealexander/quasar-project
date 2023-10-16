<template>
  <q-page>
    <div class="row q-mb-md">
      <div class="col bg-primary">1</div>
      <div class="col bg-secondary">2</div>
      <div class="col bg-accent">3</div>
      <!-- <div class="col">4</div> -->
    </div>
    <div class="row q-mb-md">
      <div class="col col-5 bg-primary">1</div>
      <div class="col bg-secondary">2</div>
      <div class="col col-6 bg-accent">3</div>
      <!-- <div class="col">4</div> -->
    </div>
    <div class="row q-mb-md justify-center">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>

      <!-- <div class="col">4</div> -->
    </div>
    <div class="row q-mb-md justify-end">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>

      <!-- <div class="col">4</div> -->
    </div>
    <div class="row q-mb-md justify-between">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>

      <!-- <div class="col">4</div> -->
    </div>
    <q-separator spaced />
    <div class="row q-mb-md justify-between">
      <div class="col-12 col-sm-6 col-md-6 bg-primary">1</div>
      <div class="col-12 col-sm-6 col-md-6 bg-secondary">2</div>

      <!-- <div class="col">4</div> -->
    </div>
    <q-separator spaced />
    <div class="row q-mb-md">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div class="row q-mb-md justify-between">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div class="row q-mb-md justify-end">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div class="row q-mb-md justify-around">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div class="column q-mb-md items-center bg-dark">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div class="column q-mb-md items-end bg-dark">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div class="column q-mb-md justify-center items-center bg-dark">
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
    <div
      class="column q-mb-md custom-height items-center justify-between bg-dark"
    >
      <div class="square-box bg-primary">1</div>
      <div class="square-box bg-secondary">2</div>
      <div class="square-box bg-accent">4</div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "FlexPage",
});
</script>
<style scoped>
.col,
.col-4,
.col-6,
.cl-12 {
  height: 50px;
}

.square-box {
  width: 50px;
  height: 50px;
}
.custom-height {
  height: 100px;
}
</style>

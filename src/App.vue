<template>
  <div  id="app">
    <div>
      <h1> {{dataRender}}</h1>
    </div>
    <div>
      <input-form  />
    </div>
    <hr>
    <div v-for="n in 2" :key="n">
      <input-form  />
    <hr>
      </div>
  </div>
</template>
<script setup >
import { ref } from "vue";
import InputForm from "./components/InputForm.vue"
const dataRender = ref();

</script>
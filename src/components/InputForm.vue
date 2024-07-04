<template>
   <div v-for="(value, key) in guestinfo" :key="key">
    <label :for="key">{{ key }}</label>
    <input :id="key" v-model="guestinfo[key]" />
    </div>
    <BottonVue  @copy="handlcopy(guestinfo)" />
    <Paste  @paste="handlpaste" :Guestinfo="guestinfo" />
</template>
<script setup>
import { ref } from "vue";
import BottonVue from "./Botton.vue";
import Paste from "./Paste.vue";

    const guestinfo = ref({
        name : "",
        date : "",
        dayofstay : 0,
    })
    const handlcopy = (data) => {
        console.log(`inputfom  ${data}`);
        guestinfo.value = data;
    }
    const handlpaste = (data) =>{
        console.log(data);
    }
  
</script>
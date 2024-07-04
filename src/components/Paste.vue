<template>
    <button @click="paste">paste</button>
</template>

<script setup>
const props = defineProps({
    Guestinfo : Object
})
    const emit = defineEmits(["paste"]);
  
    const paste= () => {
        console.log(props.Guestinfo);
        emit('paste' , props.Guestinfo)
    }


</script>
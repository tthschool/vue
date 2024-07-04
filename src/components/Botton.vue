<template>
     <button @click="copy">copi</button>
</template>
<script setup>

    const emit = defineEmits(["copy" , "paste"]);
    const copy = () => {
        emit('copy' )
        
    }
   


</script>
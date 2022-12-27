<template>
    <div class="all1">
        <h2>This is a popup</h2>
        <button @click="$emit('close')">close</button>
    </div>
</template>

<script>
export default {
    name: "PopUp",
    emit:['close']
};

</script>

<style>
     .all1{
        color: brown;
     }     
    
</style>
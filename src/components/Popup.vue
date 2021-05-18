<template>
    <div>
        <h2>This is a Popup</h2>
        <button @click="$emit('close', 'Data from child')">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name:'Popup',
        emits:['close']//emits is from vue library
    }
</script>

<style scoped>

</style>
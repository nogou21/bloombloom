<script setup lang="ts">
</script>

<template>
    <div class="card">
        <slot>default</slot>
    </div>
</template>

<style scoped>
.card{
    height: 18rem;
    width: 29.6rem;
    display: inline-block;
    text-align: center;
    line-height: 18rem;
    border-left: solid 0.05rem black;
    border-right: solid 0.05rem black;
    border-bottom: solid 0.05rem black;
}
</style>
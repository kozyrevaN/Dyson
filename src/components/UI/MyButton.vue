<template>
    <button
    style="
    background-color: #111111;
    width:220px;
    height:64px;
    border-radius:3px;
    padding:10px, 20px;
    "
    >
    <p
    style="
    color:#F8F8F8;
    weight:400;
    font-size:24px;
    padding:0px;
    margin:0px;
    "
    
    >В корзину</p>
        <slot></slot>
    </button>
</template>

<script>
    export default {
        name:'my-Button'
        
    }
</script>

<style  scoped>

</style>
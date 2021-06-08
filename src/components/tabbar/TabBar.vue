<template>
    <div id="tab-bar">
       <slot></slot>
    </div>
</template>

<script>
    export default {
        name: "TabBar"
    }
</script>

<style>
#tab-bar{
    background: #f7f7f7;
    height: 49px;
    position: fixed;
    display: flex;
    bottom: 0;
    left: 0;
    right: 0;
}
</style>
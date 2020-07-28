<template>
    <div id="tab-bar">
        <slot></slot>
    </div> 
</template>

<script>
export default {
    name:'Tabbar'
}
</script>

<style scope>
    #tab-bar{
        display: flex;
        position: fixed;
        background-color: #f6f6f6;
        bottom: 0;
        right: 0;
        left: 0;
        box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
    }
</style>
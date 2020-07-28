<template>
        <div class="tab-bar-item" @click="itemClick">
            <slot v-if="!isActive" name="item-icon"></slot>
            <slot v-else name="item-icon-active"></slot>
            <div :class="{active: isActive}"><slot name="item-text"></slot></div>
        </div>
</template>
<script>
export default {
    name:'TabBarItem',
    data() {
        return {
            // isActive: true
        }
    },
    props:{
        path: String 
    },
    methods: {
        itemClick(){
           this.$router.replace(this.path);
        }
    },
    computed: {
        isActive(){
            // 通过传过来的路劲和当前活跃路径对比来改变isActive的值
            return this.$route.path.indexOf(this.path) !== -1
        }
    },
}
</script>

<style scoped>
 .tab-bar-item{
        flex: 1;
        text-align: center;
        height: 49px;  
        font-size: 14px;  
    }
    .tab-bar-item img{
        margin-top: 2px;
        width: 24px;
        height: 24px;
    }
    .active{
        color: red;
    }
</style>
<template>
    <div id="tab-item" @click="itemClick">
        <div v-if="isActive">
            <slot name="icon-active"></slot>
        </div>
        <div v-else>
            <slot name="icon"></slot>
        </div>



        <div :class="{active:isActive}">
            <slot name="text"></slot>
        </div>
    </div>
</template>

<script>
    export default {
        name: "tabbaritem",
        props:{
            path:String
        },
        data(){
            return{
                /*isActive:true*/
            }
        },
        computed:{
            isActive(){
          return this.$route.path==this.path
            }
        },
        methods:{
            itemClick(){
                this.$router.push(this.path)
            }
        }
    }
</script>

<style>
    #tab-item{
        flex: 1;
        text-align: center;
        font-size: 14px;
        vertical-align: center;
    }
    div img{
        height: 20px;
        margin-top: 3px;


    }
    .active{
        color: red;
    }
</style>
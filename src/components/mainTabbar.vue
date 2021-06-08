<template>
    <router-view></router-view>
    <TabBar>
        <TabItem path="/home">
            <template v-slot:icon >
                <img src="@/assets/img/home.svg" alt="">
            </template>
            <template v-slot:icon-active>
                <img src="@/assets/img/nav-home-active.svg" alt="">
            </template>
            <template v-slot:text>
                <div>首页</div>
            </template>
        </TabItem>

        <TabItem path="/category">
            <template v-slot:icon path="/category">
                <img src="@/assets/img/Category.svg" alt="">
            </template>
            <template v-slot:icon-active>
                <img src="@/assets/img/Category-active.svg" alt="">
            </template>
            <template v-slot:text>
                <div>分类</div>
            </template>
        </TabItem>

        <TabItem path="/cart">
            <template v-slot:icon >
                <img src="@/assets/img/shop-car.svg" alt="">
            </template>
            <template v-slot:icon-active>
                <img src="@/assets/img/Shop-active.svg" alt="">
            </template>
            <template v-slot:text>
                <div>购物车</div>
            </template>
        </TabItem>

        <TabItem path="/profile">
            <template v-slot:icon>
                <img src="@/assets/img/mine.svg" alt="">
            </template>
            <template v-slot:icon-active>
                <img src="@/assets/img/min-active.svg" alt="">
            </template>
            <template v-slot:text>
                <div>我的</div>
            </template>
        </TabItem>
    </TabBar>
</template>

<script>
    import TabBar from '@/components/tabbar/TabBar'
    import TabItem from '@/components/tabbar/TabBarItem'
    export default {
        name: "mainTabbar",
        components:{
            TabBar,
            TabItem
        }
    }
</script>

<style scoped>

</style>
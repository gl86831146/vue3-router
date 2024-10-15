<template>
    <nav>
        <router-link to="/">首页</router-link>
        <router-link to="/articles">文章列表</router-link>
        <router-link to="/user">个人中心</router-link>
    </nav>

    <router-view v-slot="{ Component }">
        <transition name="fade" mode="out-in">
            <component :is="Component" />
        </transition>
    </router-view>
</template>

<style scoped>
a {
    margin: 10px;
    text-decoration: none;
    background-color: #3baee0;
    color: white;
    padding: 5px 10px;
    /* 修正了逗号 */
}

.router-link-active {
    background-color: #3843bb;
    font-weight: bold;
}

.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
    opacity: 0;
}
</style>
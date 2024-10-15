<template>
    <div>
        <nav>
            <router-link to="/user/profile">用户数量</router-link>
            <router-link to="/user/setting">用户设置</router-link>
        </nav>
        <router-view></router-view>
    </div>
</template>

<style scoped>
nav{
    margin-top: 20px;
}
a {
    margin: 10px;
    text-decoration: none;
    background-color: #3baee0;
    color: white;
    padding: 5px, 10px;
}

.router-link-active {
    background-color: #3843bb;
    font-weight: bold;
}
</style>
<template>
    <div>
        <h2>用户信息设置</h2>
        <button @click="handleLogout">退出登录</button>
    </div>
</template>

<script lang="ts" setup>
import {useRouter} from "vue-router";
const router = useRouter();

const handleLogout = () => {
    localStorage.removeItem("token");
    router.push("/login");
};
</script>
<template>
    <div>
        <h3>用户登录</h3>
        <button @click="handleLogin">登录</button>
    </div>
</template>

<script setup lang="ts">
import { useRouter } from"vue-router";
const router=useRouter();
const handleLogin= () => {// 模拟登录成功
  localStorage.setItem("token","hello123");
  router.push("/user/profile");
};
</script>
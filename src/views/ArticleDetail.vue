<template>
    <div>
        <h2>{{ article.title }}</h2>
        <p>{{ article.content }}</p>
        <div style="height: 150px">
            <!-- 占位，模拟⻓⻚面 -->
            <p>更多的文章内容，让⻚面足够⻓。</p>
        </div>
        <router-link :to="`/articles/${article.id}/comments`">查看评论</router-link>
        <router-view></router-view>
    </div>
</template>

<script setup lang="ts">
import { useRoute } from "vue-router";

const route = useRoute();
const articleId = route.params.id;

const articles = [
    {
        id: 1,
        title: "如何学习 Vue3",
        content:
        "如何学习 Vue3 如何学习 Vue3 如何学习 Vue3",
    },
    {
        id: 2,
        title: "理解 Vue Router",
        content:
        "理解 Vue Router 理解 Vue Router 理解 Vue Router",
    },
];

const article = articles.find((a) => a.id === Number(articleId));
</script>

<style scoped></style>
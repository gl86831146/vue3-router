<template>
        <ul>
            <li v-for="comment in article.comments" :key="comment.id">
                {{ comment.content }}
            </li>
        </ul> 
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
        comments: [
            { 
                id: 1, content: "Vue 3语法很简洁"
             },
            { 
                id: 2, content: "Vue 3语法很强大" 
            },
        ],
    },
    {
        id: 2,
        title: "理解 Vue Router",
        content: 
        "理解 Vue Router 理解 Vue Router 理解 Vue Router",
        comments: [
            { 
                id: 1, content: "Vue Router基础与静态路由" 
            },
            {
                 id: 2, content: "动态路由与嵌套路由" },
        ],
    },
];

const article = articles.find((a) => a.id === Number(articleId));  
</script>

<style scoped></style>
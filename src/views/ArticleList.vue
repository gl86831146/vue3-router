<template>
    <div>
        <h2>文章列表</h2>
        <div style="height: 200px">
            <!-- 占位，模拟⻓⻚面 -->
            <p>这里是非常⻓的⻚面内容。</p>
        </div>
            <ul>
                <li v-for="article in articles" :key="article.id">
                    <router-link :to="`/articles/${article.id}`">
                        {{ article.title }}
                    </router-link>
                </li>
            </ul>
    </div>
</template>

<script lang="ts" setup>
const articles = [
    {
        id :1,
        title: "如何学习 Vue3"
    },
 {
        id: 2,
        title: "理解 Vue Router"
    },
];
</script>
<script lang="ts">
export default {
    beforeRouteEnter(to, from, next) {
        console.log(to, from);
        console.log("进入该⻚面之前的检查");
        next();  
      },
    };
</script>
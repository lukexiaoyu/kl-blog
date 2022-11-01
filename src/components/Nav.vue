<script setup>
import {ref,reactive,computed} from 'vue'
const adds=[
    {name:'Home',link:'/'},
    {name:'每日计划',link:'/everyday'},
]
</script>
<template>
<div>
    <template v-for="x in adds">
    <a :href="x.link">{{x.name}}</a>
    </template>
</div>
</template>
<style scoped>
a{
    margin: 1px;
    text-decoration: none;
}
a:hover{
    background-color: black;
    color: white;
}
</style>
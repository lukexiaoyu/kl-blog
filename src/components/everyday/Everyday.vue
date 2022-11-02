<script setup>
import {ref,reactive,computed} from 'vue'
const url = "https://cloudapi.klpalace.cn/1.1/classes/everyday";
const res=await fetch(url, {
    method: 'GET',
    headers: {
        'X-LC-Id': 'bEiFShXmGcKGJzkIItqURHOv-gzGzoHsz',
        'X-LC-Key': 'weFzyQ1fE68f61jHamXuAHcG',
        'Content-Type': 'application/json'
    }
})
const data=await res.json()
console.log(data);

function do_num() {
    let today=new Date()
    let do_day=new Date('2021-6-30')
    return today-da_day
}
const state=reactive({
    today:''
})
</script>
<template>
<div>
<template v-for="x in data.results">    
    <p>{{x.item_name}}</p>

</template>
<hr>
<input type="text" v-model="state.today">
<p>{{state.today}}</p>
</div>
</template>
<style scoped></style>
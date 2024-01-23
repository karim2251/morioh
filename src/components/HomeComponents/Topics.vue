<template>
  
  <div v-for="c in data" :key="c" class="card">Card {{ c }}</div>
</template>

<script>
export default {
   props:['data'],
   
}
</script>

<style>

</style>
<template>
       <div class="center-left">
            <div v-for="c in 5" :key="c" class="post">
                post
            </div>
       </div>
   
</template>

<script>
export default {

}
</script>

<style scoped>
.center-left{
  width: 70%;
}
.post{
  height: 300px;
  border-radius: 10px;
  width: 100%;
  border: 2px dashed transparent;
  margin-bottom: 10px;
  background-color: #1f2937;

}
.post:hover {
  border: 2px dashed #3b82f6;
  
}
</style>
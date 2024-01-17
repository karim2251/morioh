<template>
  <div class="container">

      <!-- the header div -->
    <div class="header">
      <Header />
    </div>

      <!-- the content or body -->
    <div class="content">

      <!-- the left div -->
      <div class="left">
        
        <Sidebar />
        
      </div>

      <!-- the center div -->
      <div class="center">
        <div class="c1">c1</div>
      </div>

      <!-- the right div -->
      <div class="right">
        <div class="r1">r1</div>
        <div class="r2">r2</div>
       
      </div>

    </div> <!-- the content end --> 
  </div> <!-- the container end -->
</template>

<script>
import Header from './components/Header.vue';
import Sidebar from './components/Sidebar.vue';
export default {
    components:{
      Header,
      Sidebar
    }
}
</script>

<style scoped>

.container{
  position: relative;
  display: flex;
  flex-direction: column;
  /* height: 100vh; */
  width: 100%;
  gap: 15px;
  background-color: #111827;
}
.header{
  height: 60px;
  width: 100%;
  background-color: #1f2937;
  position: sticky;
  top: 0px;
  z-index: 100;
  display: flex;
  justify-content: space-between;
}

.content{
  flex: 1;
  width: 100%;
  display: flex;
  flex-direction: row;
  gap: 20px;
  background-color: #111827;
 
  z-index: 0;
 
}

/* the left div */
.left{
  color: white;
  background-color: #111827;
  width: 280px;
  overflow-y:auto;
  display: flex;
  justify-content: end;  

  & div{
    border-radius: 10px;
    width: 86%;
    height: 60%;
    }
}

/* the center div */
.center{
  color: white;
  flex: 1 0 auto;
  width: 500px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  
  /* background-color: #1f2937; */
  & div{
    border-radius: 10px;
    width: 100%;
    border: 2px dashed transparent;
    
  }
  & div:hover{
    border:2px dashed #3b82f6;
    border-radius: 10px;
    width: 100%;
  }
}
.c1{
  color: white;
  background-color: #1f2937;
  height:900px;
}


/* the right div */
.right{
  display: flex;
  flex-direction: column;
  color: white;
  /* background-color: #1f2937; */
  width: 360px;
  overflow-y:auto;
  gap: 15px;

  & div{
    /* border: 2px dashed transparent; */
    border-radius: 10px;
    width: 86%;
    color: white;
    background-color: #1f2937;
    height: 60%;
  }
  
}


</style>
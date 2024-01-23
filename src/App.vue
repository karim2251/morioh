<template>
    <!-- the header div -->
      <Header />

    <!-- the content or body -->
    <div class="content">
      <span>
      <Sidebar />

      <div class="center">
          <Posts/>
          <Followers/>
        
      </div>
    </span>
      <!-- <Home /> -->
    </div>
    <!-- the content end -->

</template>

<script>
import Header from "./views/Header.vue";
import Sidebar from "./components/Sidebar.vue";
import Home from "./views/Home.vue";
import Posts from "./components/Posts.vue";
import Followers from "./components/Followers.vue";
export default {
  components: {
    Header,
    Sidebar,
    Home,
    Posts,
    Followers
  },
  data(){
    return{
      
    }
  }
};
</script>

<style scoped>
 
.content {
  position: relative;
  width: 100%;
  overflow: hidden;
  background-color: #111827;
 
}
/* the center div */
.center {
  color: white;
  width: 80%; 
  margin: 1% 20%;
  display: flex;
  gap: 20px;
}


</style>
<template>
  <!-- <div class="container"> -->
    <!-- the header div -->
      <Header />

    <!-- the content or body -->
    <div class="content">

      <!-- the left div -->
      <!-- <Sidebar /> -->

      <!-- the center div -->
      <!-- <div class="center">
        <div class="c1">c1</div>
      </div> -->

      <!-- the right div -->
      <!-- <div class="right">
        <div class="r1">r1</div>
        <div class="r2">r2</div>
      </div> -->

      <Home />
    </div>
    <!-- the content end -->
  <!-- </div> -->
  <!-- the container end -->
</template>

<script>
import Header from "./components/Header.vue";
import Sidebar from "./components/Sidebar.vue";
import Home from "./components/Home.vue";
export default {
  components: {
    Header,
    Sidebar,
    Home,
  },
};
</script>

<style scoped>
 
.content {
  flex: 1;
  width: 100%;
  display: flex;
  flex-direction: column;/* here */
  gap: 20px;
  background-color: #111827;
}

/* the center div */
.center {
  color: white;
  flex: 1 0 auto;
  /* here */
  margin-left: 22%;
  margin-right: 28%;
  /* ======= */
  width: 500px;
  display: flex;
  flex-direction: column;
  gap: 15px;

  /* background-color: #1f2937; */
}
.center div {
  border-radius: 10px;
  width: 100%;
  border: 2px dashed transparent;
}
.center div:hover {
  border: 2px dashed #3b82f6;
  border-radius: 10px;
  width: 100%;
}
.c1 {
  color: white;
  background-color: #1f2937;
  height: 900px;
}

/* the right div */
.right {
  /* here */
  position: fixed;
  top: 75px;
  right: 0px;
  /* ======== */
  display: flex;
  flex-direction: column;
  color: white;
  width: 360px;
  overflow-y: auto;
  gap: 15px;
}

.right div {
  border-radius: 10px;
  width: 86%;
  color: white;
  background-color: #1f2937;
  /* here */
  height: 400px;
}
</style>
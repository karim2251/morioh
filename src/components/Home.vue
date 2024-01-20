<template>
  <div class="home_header">
    <div class="home_header_left">
      <h1>Social Network</h1>
      <h2>for Programmers and Developers</h2>
      <p>
        The era of Web 3.0 is coming, the digital economy is a radical new
        imagining of the future of work. We want to promote this vision by using
        the power of <b> blockchain, crowd knowledge </b> and <b> mass collaboration</b> to
        provide access to the global sharing economy to connect the talents of
        millions of programmers and developers around the world.
      </p>
      <p>Be the pioneer of the future.</p>
    </div>
    <div class="home_header_right">2</div>
  </div>
  <div class="home_content">

  <div class="playground">
    <h1> # playground</h1>
    <div v-for="c in cpt1" :key="c" class="card">Card {{ c }}</div>
   
  </div>

  <div class="topics">
    <div v-for="c in cpt2" :key="c" class="card">Card {{ c }}</div>

  </div>opics
  
  </div>
</template>

<script>
export default {
data() {
  return {
    cpt1: 6,
    cpt2: 8,
  };
},
};
</script>

<style scoped>
.home_header {
  display: flex;
  flex-direction: row;
  width: 100%;
  gap: 20px;
}
.home_header_left {
  flex: 1 0 auto;
  width: 60%;
  color: rgb(204, 204, 204);
  text-align: left;
  padding: 150px 0px 70px 50px;  
  line-height: 0.6;

}
.home_header_left h1 {
  font-size: 50px;
  font-weight: 700;
}
.home_header_left h2 {
  font-size: 35px;
  font-weight: 600;
  background: linear-gradient(to right, #3498db, #9b59b6);
  background-clip: text;
  padding: 5px 0px 5px 0px;
  color: transparent;
  line-height: 1.5;
  
  
}
.home_header_left p {
  font-size: 20px;
  font-weight: 400;
  line-height: 1.5;
}
.home_header_right {
  background-color: aqua;
  width: 40%;
}

/* playground */
.playground {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 20px;
  background-color: #1f2937;
  /* height: 100vh; */
}
.playground h1{
    font-size: 30px;
    font-weight: 600;
    margin-bottom: 20px;
    width: 100%;
    text-align: start;
    padding-left: 20px;
    background: linear-gradient(to right, #3498db, #9b59b6);
    background-clip: text;
    color: transparent;
    text-transform: capitalize;
  
  }
.playground .card {
  flex: 0 1 calc(33.33% - 20px); 
  margin: 10px;
  padding: 20px;
  box-sizing: border-box;
  background-color: #f0f0f0;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: center;
  height: 200px;
}

/* topics */

.topics {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 20px;
  background-color: #111827;
  color: white;
}
.topics .card{
  flex: 0 1 calc(25% - 20px);
  margin: 10px;
  padding: 10px;
  box-sizing: border-box;
  background-color: #1f2937;
  border: 1px solid #ddd;
  border-radius: 8px;
  text-align: start;
  height: 70px;

}


@media screen and (max-width: 970px) {
  .playground .card {
    flex: 0 1 calc(50% - 20px); 
  }
  .home_header_right{
    display: none;
  }
  .home_header_left{
  padding: 50px 0px 70px 50px;  

  }
}
@media screen and (max-width: 600px) {
  .playground .card {
    flex: 0 1 calc(90% - 20px); 
  }

}
</style>
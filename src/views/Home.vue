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
   <Playground :data="cpt1"/>
  </div>

  <div class="topics">
    <h1># topics</h1>
      <Topics :data="cpt2"/>

  </div>

  <div class="share_to_learn">

      <h1>Share to Earn</h1>
      <p>Let's write, share knowledge and earn <b>GEEK</b> coin.</p>
      <button id="join">join now</button>


  </div>
  
  </div>

  <footer>
    <div class="des">
          <h2>morioh</h2>
          <p>Social network for developers to discuss topics about
            bugs and issues, share knowledge and connect the 
            talents of millions of programmers and developers 
            around the world.
          </p>
          <div class="links">
            <a href="#"><FacebookIcon/></a>
            <a href="#"><TwitterIcon/></a>
            <a href="#"><DiscordIcon/></a>
            <a href="#"><GithubIcone/></a>
            <a href="#"><EmailIcon/></a>
          </div>
    </div>
    
    <div class="earn">
          <h3>EARN</h3>
          <div class="links">
            <a href="#">what is GEEK?</a>
            <a href="#">how to earn</a>
            <a href="#">referral program</a>
            <a href="#">how to staking</a>
            <a href="#">build a validator</a>
          </div>

    </div>
    <div class="resources">
      <h3>RESOURCES</h3>
          <div class="links">
            <a href="#">Password Generator</a>
            <a href="#">Code to Image</a>
            <a href="#">JavaScript Minify and Beautify</a>
            <a href="#">HTML Minify and Beautify</a>
            <a href="#">QR Code Generator</a>
            <a href="#">HTML to Markdown</a>
          </div>
    </div>

    <div class="learn">
      <h3>LEARN</h3>
          <div class="links">
            <a href="#">Fullstack Web3 Development</a>
            <a href="#">Learn Python from Harvard University</a>
            <a href="#">TypeScript Crash Course</a>
            <a href="#">React Tutorial for Beginners</a>
            <a href="#">Next.js Crash Course</a>
          </div>

    </div>

    





  </footer>
</template>

<script>
import DiscordIcon from '../components/icons/DiscordIcon.vue';
import EmailIcon from '../components/icons/EmailIcon.vue';
import FacebookIcon from '../components/icons/FacebookIcon.vue';
import GithubIcone from '../components/icons/GithubIcone.vue';
import TwitterIcon from '../components/icons/TwitterIcon.vue';
import Topics from '../components/HomeComponents/Topics.vue';
import Playground from '../components/HomeComponents/Playground.vue';
export default {
  components:{
    DiscordIcon,
    EmailIcon,
    FacebookIcon,
    GithubIcone,
    TwitterIcon,
    Topics,
    Playground
  },
data() {
  return {
    cpt1: 6,
    cpt2: 8,
  };
},
};
</script>

<style >
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
  border-radius: 8px;
  text-align: center;
  height: 200px;
  outline: 2px dashed transparent;
}
.playground .card:hover{

  outline: 2px dashed #3b82f6;
  

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
  border-radius: 8px;
  text-align: start;
  height: 70px;
  outline: 2px dashed transparent;

}
.topics .card:hover{

  outline: 2px dashed #3b82f6;

}
.topics h1{
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

/* share_to_learn */

.share_to_learn{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: #1f2937;
  color: white;
  background-image: url('../assets/course-graphics.svg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
  height: 350px;
  font-size: 20px;
}
.share_to_learn h1{
  background: linear-gradient(to right ,#3498db,#9b59b6);
  background-clip: text;
  color: transparent;
  margin-bottom: -5px;
}
.share_to_learn p{
  font-size: 18px;
  word-spacing: 1.5px;
}
#join{
  border-radius: 10px;
  width: 90px;
  height: 40px;
  background-color: #3b82f6;
  outline: 2px dashed transparent;
  border: none;
  color: white;
  font-size: 16px;
  font-weight: 200;
}

#join:hover{
  background-color: #2563eb;
  outline: 2px dashed #3b82f6;
}

/* footer */

footer{
  display: flex;
  color: white;
  gap: 10px;
  width: 100%;
}
/* des div */
footer .des{
  flex: 0 1 calc(40% - 10px);
  display: flex;
  flex-direction: column;
  text-align: start;
  padding: 50px;
}

footer .des h2{
  background: linear-gradient(to right,#3498db,#9b59b6);
  background-clip: text;
  color: transparent;
  text-transform: capitalize;
}
footer .des p{
  font-size: 15px;
  color: #6b7280;
  line-height: 1.5;
}
footer .des .links{
  display: flex;
  justify-content:space-between;
  width: 50%;
}
footer .des .links a{
  font-size: 25px;
  color: #6b7280;
}
footer .des .links a:hover{
  font-size: 25px;
  color: white;
}

/* earn & resources & learn divs */

footer .earn , .resources , .learn{
  display: flex;
  flex-direction: column;
  padding: 55px 0px 0px 0px;
  text-align: start;
  padding-bottom: 50px;
}
footer :is(.earn,.resources,.learn) h3 {
  color: #6b7280;
}
footer :is(.earn,.resources,.learn) .links{
  display: flex;
  flex-direction: column;
  gap: 15px;
}
footer :is(.earn,.resources,.learn) .links a{
  text-decoration: none;
  font-size: 16px;
  color:#6b7280;
  text-transform: capitalize;
}
footer :is(.earn,.resources,.learn) .links a:hover{
  color: white;
}



footer div:not(.des){
  flex: 0 1 calc(25% - 10px);
}






@media screen and (max-width: 1024px) {
  
  footer{
    flex-wrap: wrap;
    justify-content: center;
  }
  footer .des{
    flex: 0 1 calc(90% - 10px); 

  }
  footer div:not(.des){
  flex: 0 1 calc(30% - 10px);
}

}

@media screen and (max-width: 970px) {
  :is(.playground,.topics) .card {
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
  :is(.playground,.topics) .card {
    flex: 0 1 calc(90% - 20px); 
  }
  
  footer div:not(.des){
  flex: 0 1 calc(90% - 10px);
  text-align: center;
  padding-bottom: 0px;
}
footer .learn{
  padding-bottom: 50px !important;
}

footer :is(.earn,.resources,.learn)::before{
  content: ' ';
  border: 1px solid #6b7280;

}

}
</style>
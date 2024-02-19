<template>
       <div class="center-left">
            <div class="post" v-for="c in 5" :key="c">
              <div class="head_post">
                <span>
                <a class="image_head_post" href="#">
                   <img src="../assets/karim.png" alt="" />
                </a>
                <div class="name_the_user">
                  <a href="#">the name of user</a>
                  <p>2 hour ago</p>

                </div>
              </span>
                <div class="option">
                  <button>
                    <DotOptions />
                  </button>
                </div>
              </div>
              <div class="body_post">

                <div class="markdown">
                  <h2>the content here</h2>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio doloremque commodi ab magni esse eius expedita minima voluptates ullam recusandae numquam, tempora molestiae eos temporibus vitae aliquam! Vitae ut consectetur nulla possimus ratione? Eaque totam ex soluta laudantium debitis molestiae impedit quam at libero quae aut quo cumque nam sequi hic delectus explicabo aperiam ducimus, odio voluptatum quisquam voluptates reiciendis atque repellendus! Fuga rerum suscipit ullam quia repudiandae ratione quibusdam aut, officiis doloribus quis, vero veritatis in culpa nostrum. Aspernatur animi autem nostrum ea harum qui recusandae. Fugit laudantium quod corporis quos quibusdam esse ipsum eaque vitae quidem, nesciunt accusamus!</p>
                </div>
                <div class="photo">
                  <img src="../assets/post.webp" alt="" />
                </div>

              </div>
              <div class="footer_post">
                <div class="like_comment">
                  <button>
                    <LikeIconVue />
                  </button>
                  <button @click="showCommentfun">
                    <CommentIconVue />
                  </button>
                </div>
                <div class="share">
                  <button>
                    <ShareIcon />
                  </button>
                </div>
              </div>
              <div v-if="showComment" class="comment_input">
                <span>
                  <img src="../assets/karim.png" alt=""  />
                </span>
                <input type="text" placeholder="write a comment">
              </div>

            </div>
       </div>
   
</template>

<script>
import DotOptions from './icons/3DotOptions.vue';
import CommentIconVue from './icons/CommentIcon.vue';
import LikeIconVue from './icons/LikeIcon.vue';
import ShareIcon from './icons/ShareIcon.vue';
export default {
  data(){
    return{
      showComment:false
    }
  },
components:{
  DotOptions,
  LikeIconVue,
  ShareIcon,
  CommentIconVue
},
methods:{
  showCommentfun(){
    this.showComment = ! this.showComment
  }
}
}
</script>

<style scoped>
.center-left{
  width: 70%;
}
.post{
  /* height: 300px; */
  border-radius: 10px;
  width: 100%;
  border: 2px dashed transparent;
  margin-bottom: 10px;
  background-color: #1f2937;
  position: relative;

}
.post:hover {
  border: 2px dashed #3b82f6;
  
}
.post .head_post {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.post :is(.head_post .image_head_post,.comment_input span) {
  height: 40px;
  width: 40px;
  border-radius: 50%;
  border: none;
  background-color: #474f5b;
  color: white;
  font-size: 16px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 10px;  
}

.post :is(.head_post .option,.footer_post .like_comment ,.footer_post .share) button{
  display: flex; 
  justify-content: center; 
  align-items: center;
  border: none;
  background-color: #1f2937;
  color: white;
  font-size: 25px;
  cursor: pointer;
  border-radius: 50% ;
  padding: 5px;
  position: relative;
  right: 10px;
  
}
.post :is(.head_post .option,.footer_post .like_comment ,.footer_post .share) button:hover{
  background-color: #111827;

}
.post :is(.head_post .image_head_post, .comment_input span) img {
  width: 40px;
  border-radius: 50%;
  
}
.post .head_post .name_the_user{

display: flex;
justify-content: start;
flex-direction: column;
position: absolute;
top: 20px;
left: 60px;
text-align: start;
 
}
.post .head_post .name_the_user a{

  color: white;
  text-decoration: none;
  text-transform: capitalize;
  line-height: 0.3;
}
.post .head_post .name_the_user p{
  font-size: 13px;
  color: rgb(136, 133, 133);
}

.post .body_post .markdown{
  text-align: start;
  padding: 0px 10px;
}
.post .body_post .photo img{
  width: 100%;
}
.post .footer_post {
  display: flex;
  justify-content:space-between;
  align-items: center;
  padding:20px ;
}
.post .footer_post button{
  color: rgba(184, 179, 179, 0.699) !important;
  font-size: 25px !important;
}
.post .footer_post .like_comment {
  display: flex;
  /* justify-content:space-evenly; */
  align-items: center;
  flex-direction: row ;
  gap: 15px;
  position: relative;
  left: 20px;
}
.post .comment_input{
  padding: 0px 20px;
  display: flex;
  align-items: center;
  gap: 10px;
  padding-bottom: 10px;
}
.post .comment_input input{
  height: 40px;
  width: 70%;
  background-color: #474f5b;
  border: none;
  outline: 2px dashed transparent;
  border-radius: 5px;
  color: white;
  font-size: 16px;
  padding: 0px 10px;
}
.post .comment_input input:hover{
  outline: 2px dashed #3b82f6;

}
</style>
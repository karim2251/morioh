<template>
    <div class="header">
  <div class="header_left">
    <a href="#">
      <img src="../assets/logo.png" alt="" />
    </a>
    <hr />
    <SearchIcon :showicon="showicon" @click="showinput" class="searchicon"/>
    <input type="text" id="search" ref="search" placeholder="Search..." />
    <kbd class="keyboard-key">⌘K</kbd>
  </div>
  

  <div v-if="shownav" class="header_right">
    <button title="new post">
      <PostsIcon/>
    </button>
    <button>
      <NotificationIcon/>
    </button>
    <button>
    <WalletIcon/>
    </button>

    <!-- profill -->
    <button @click="dropdownfun">
      <img src="../assets/karim.png" alt="" />
    </button>

    <!-- dropdown -->
    <Dropdown :dropdownshow="dropdownshow" />
    
  </div>
  <div v-else class="header_right">
      <button id="login">Sign up</button>
  </div>
 
  
  
  </div>

</template>

<script>
import Dropdown from '../components/Dropdown.vue';
import NotificationIcon from '../components/icons/NotificationIcon.vue';
import PostsIcon from '../components/icons/PostsIcon.vue';
import WalletIcon from '../components/icons/WalletIcon.vue';
import SearchIcon from '../components/icons/SearchIcon.vue';
export default {
  components:{
    Dropdown,
    PostsIcon,
    NotificationIcon,
    WalletIcon,
    SearchIcon,
    
  },
  data() {
    return {
      shownav: true,
      dropdownshow:false,
      showicon:false,
      
    };
  },
  methods:{
    focusinput(event){
      if(event.metaKey && event.key === 'k'){
        this.$refs.search.focus()
        
      }

    },
    dropdownfun(){
      this.dropdownshow = !this.dropdownshow
    },
    showinput(){
      this.$refs.search.classList.toggle('showinput')
      this.showicon = !this.showicon

    }

  },
  mounted(){
    window.addEventListener('keyup',this.focusinput);
  },
  
};
</script>

<style scoped>

.header {
  height: 60px;
  width: 100%;
  background-color: #1f2937;
  position: sticky;
  top: 0px;
  z-index: 100;
  display: flex;
  justify-content: space-between;
}
.header_left {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.header_left hr {
  height: 20px;
  border: none;
  border-left: 1px solid #979595;
}

.header_left input {
  height: 60%;
  width: 350px;
  border-radius: 5px;
  border: none;
  outline: none;
  background-color: #474f5b;
  color: white;
  margin-left: 15px;
  padding-left: 10px;
  border: 2px dashed transparent;
  font-size: 16px;
}
.header_left input::placeholder {
  color: #abb4c4af;
  font-size: 16px;
}
/* input:hover{
     border:2px dashed #3b82f6;
  } */
input:focus {
  border: 2px dashed #3b82f6;
}
.searchicon{
  color: white;
  position: absolute;
  left: 80px;
  display: none;
}
.header_right {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.header_right button {
  height: 40px;
  width: 40px;
  border-radius: 50%;
  /* outline: none; */
  border: none;
  background-color: #474f5b;
  color: white;
  font-size: 16px;
  cursor: pointer;
  margin: 0px 10px 0px 0px;
  outline: 1px dashed transparent;
  display: flex;
  justify-content: center;
  align-items: center;
  
}
.header_right button svg {
  height: 20px;
  width: 20px;
}
.header_right button:hover {
  outline: 3px dashed #3b82f6;
}

.header_right button img {
  width: 40px;
  border-radius: 50%;
}
#login{
  border-radius: 10px;
  width: 90px;
  background-color: #3b82f6;
}
#login:hover{
  background-color: #2563eb;
}
.showinput{
  display: block !important;
}
.keyboard-key {
      display: inline-flex;
      align-items: center;
      border: 1px solid rgba(156, 163, 175, 0.4);
      border-radius: 0.375rem; /* Equivalent to 6px */
      padding: 5px 10px;
      position: relative;
      left: -55px;
      font-family: sans-serif;
      font-weight: 500;
      color: #8e9aac;
      background-color: #474f5b;
      
       /* Text color */
    }

    /* .moveSearch{

      display: inline !important;
      position: relative !important;
      top: 60px !important;
    }
    */

  @media screen and (max-width: 699px) {
    .header_right button:nth-of-type(-n+3){
      display: none;
    }
    

  }
  @media screen and (max-width: 600px) {
  .header_left{
      position: relative;
      left: 40px;
    }
      .header_left input{
        position: absolute;
        left: -15px;
        top: 80px;
        display: none;

      }
      .keyboard-key{
    display: none;
   }
   .searchicon{
    display: block;
   }
  }
  @media screen and (max-width: 570px) {
   
    #search{
    width: 290px;

  } 
  
  }
</style>
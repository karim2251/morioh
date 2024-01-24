<template>
    <div class="header">
  <div class="header_left">
    <a href="#">
      <img src="../assets/logo.png" alt="" />
    </a>
    <hr />
    <input type="text" id="search" ref="search" placeholder="Search..." />
    <kbd class="keyboard-key">⌘K</kbd>
  </div>

  <div v-if="shownav" class="header_right">
    <button>
      <svg
        stroke="currentColor"
        fill="currentColor"
        stroke-width="0"
        viewBox="0 0 24 24"
        class="h-5 w-5"
        aria-hidden="true"
        height="1em"
        width="1em"
        xmlns="http://www.w3.org/2000/svg"
        data-darkreader-inline-fill=""
        data-darkreader-inline-stroke=""
        style="
          --darkreader-inline-fill: currentColor;
          --darkreader-inline-stroke: currentColor;
        "
      >
        <path
          d="M19.045 7.401c.378-.378.586-.88.586-1.414s-.208-1.036-.586-1.414l-1.586-1.586c-.378-.378-.88-.586-1.414-.586s-1.036.208-1.413.585L4 13.585V18h4.413L19.045 7.401zm-3-3 1.587 1.585-1.59 1.584-1.586-1.585 1.589-1.584zM6 16v-1.585l7.04-7.018 1.586 1.586L7.587 16H6zm-2 4h16v2H4z"
        ></path>
      </svg>
    </button>
    <button>
      <svg
        stroke="currentColor"
        fill="currentColor"
        stroke-width="0"
        viewBox="0 0 24 24"
        class="h-5 w-5"
        aria-hidden="true"
        height="1em"
        width="1em"
        xmlns="http://www.w3.org/2000/svg"
        data-darkreader-inline-fill=""
        data-darkreader-inline-stroke=""
        style="
          --darkreader-inline-fill: currentColor;
          --darkreader-inline-stroke: currentColor;
        "
      >
        <path
          d="M19 13.586V10c0-3.217-2.185-5.927-5.145-6.742C13.562 2.52 12.846 2 12 2s-1.562.52-1.855 1.258C7.185 4.074 5 6.783 5 10v3.586l-1.707 1.707A.996.996 0 0 0 3 16v2a1 1 0 0 0 1 1h16a1 1 0 0 0 1-1v-2a.996.996 0 0 0-.293-.707L19 13.586zM19 17H5v-.586l1.707-1.707A.996.996 0 0 0 7 14v-4c0-2.757 2.243-5 5-5s5 2.243 5 5v4c0 .266.105.52.293.707L19 16.414V17zm-7 5a2.98 2.98 0 0 0 2.818-2H9.182A2.98 2.98 0 0 0 12 22z"
        ></path>
      </svg>
    </button>
    <button>
      <svg
        stroke="currentColor"
        fill="currentColor"
        stroke-width="0"
        viewBox="0 0 24 24"
        class="h-5 w-5"
        aria-hidden="true"
        height="1em"
        width="1em"
        xmlns="http://www.w3.org/2000/svg"
        data-darkreader-inline-fill=""
        data-darkreader-inline-stroke=""
        style="
          --darkreader-inline-fill: currentColor;
          --darkreader-inline-stroke: currentColor;
        "
      >
        <path
          d="M20 3H5C3.346 3 2 4.346 2 6v12c0 1.654 1.346 3 3 3h15c1.103 0 2-.897 2-2V5c0-1.103-.897-2-2-2zM5 19c-.552 0-1-.449-1-1V6c0-.551.448-1 1-1h15v3h-6c-1.103 0-2 .897-2 2v4c0 1.103.897 2 2 2h6.001v3H5zm15-9v4h-6v-4h6z"
        ></path>
      </svg>
    </button>
    <button>
      <img src="../assets/karim.png" alt="" />
    </button>

    
  </div>
  <div v-else class="header_right">
      <button id="login">Sign up</button>
  </div>
  <div class="dropdown">
      <p>dcdacdc</p>
    </div>  
  </div>

</template>

<script>
export default {
  data() {
    return {
      shownav: true,
      
    };
  },
  methods:{
    focusinput(event){
      if(event.metaKey && event.key === 'k'){
        this.$refs.search.focus()
        
      }
      

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
      
       /* Text color */
    }

    /* .moveSearch{

      display: inline !important;
      position: relative !important;
      top: 60px !important;
    }
    */
.dropdown{
  /* display: none; */
  position: absolute;
  color: white;
  top: 70px;
  right: 20px;
  z-index: 200;
}
  @media screen and (max-width: 699px) {
    .header_right button:not(:last-child){
      display: none;
    }

  }
  @media screen and (max-width: 570px) {
    #search{
    /* display: none; */
    width: 150px;

  } 
  .keyboard-key{
    display: none;
   }
  }
</style>
<template>
  <div class="left">
    <div class="links">
      <a href="#">
        <FeedIcon />
        <span>feed</span>
      </a>
      <a href="#">
        <PopilarIcon />
        <span>popilar</span>
      </a>
      <a href="#">
        <RecentsIcon />
        <span>recents</span>
      </a>
      <a href="#">
        <VideosIcon />
        <span>videos</span>
      </a>
      <a href="#">
        <QuestionsIcon />
        <span>questions</span>
      </a>

      <!-- hidden links -->

      <a href="#" class="hide">
        <MessagesIcon />
        <span>messages</span>
      </a>
      <a href="#" class="hide">
        <TopicsIcon />
        <span>topics</span>
      </a>
      <a href="#" class="hide">
        <ListsIcon />
        <span>lists</span>
      </a>
      <a href="#" class="hide">
        <GroupsIcon />
        <span>groups</span>
      </a>
      <a href="#" class="hide">
        <MarketplaceIcon />
        <span>marketplace</span>
      </a>
      <a href="#" class="hide">
        <JobsIcon />
        <span>jobs</span>
      </a>
    </div>
  </div>
</template>

<script>
import FeedIcon from "./icons/FeedIcon.vue";
import PopilarIcon from "./icons/PopilarIcon.vue";
import RecentsIcon from "./icons/RecentsIcon.vue";
import VideosIcon from "./icons/VideosIcon.vue";
import QuestionsIcon from "./icons/QuestionsIcon.vue";
import MessagesIcon from "./icons/MessagesIcon.vue";
import TopicsIcon from "./icons/TopicsIcon.vue";
import ListsIcon from "./icons/ListsIcon.vue";
import GroupsIcon from "./icons/GroupsIcon.vue";
import MarketplaceIcon from "./icons/MarketplaceIcon.vue";
import JobsIcon from "./icons/JobsIcon.vue";

export default {
  components: {
    FeedIcon,
    PopilarIcon,
    RecentsIcon,
    VideosIcon,
    QuestionsIcon,
    MessagesIcon,
    TopicsIcon,
    ListsIcon,
    GroupsIcon,
    MarketplaceIcon,
    JobsIcon,
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
/* the left div */
.left {
  color: white;
  background-color: #111827;
  width: 270px;
  float: left;
  overflow-y: auto;
  display: flex;
  justify-content: center;
  position: fixed;
  top: 10%;
  left: 0;
  bottom: 0;
}
.left::-webkit-scrollbar {
  display: none;
}
.left div {
  border-radius: 10px;
  width: 90%;
}

.links {
  display: flex;
  flex-direction: column;
  gap: 5px;
  padding: 10px 0px;
}
.links a {
  display: flex;
  align-items: center;
  justify-content: start;
  gap: 10px;
  padding: 10px 20px;
  color: #fff;
  text-decoration: none;
  font-size: 1rem;
  text-transform: capitalize;
}
.links a:hover {
  background-color: #4e576394;
  border-radius: 10px;
}
.links a svg {
  width: 23px;
  height: 23px;
  color: #b6b2b2;
}

.hide {
  opacity: 0.6;
  cursor: wait;
}
@media screen and (max-width: 1355px) {
  .left {
 
    width:200px;

  }
  
}
@media screen and (max-width: 1024px) {

  .left {
    top: 9.5%;
    width:190px;
    padding-top: 10px;


  }
  
}

@media screen and (max-width: 970px) {
  .left .links a span {
    display: none;
  }
  .left {
    top: 8%;
    width: min-content;
    padding-left:10px;
    display: block;
    padding-top: 20px;
  }
  .links a{
  padding: 2px 20px;

    
  }
}
</style>
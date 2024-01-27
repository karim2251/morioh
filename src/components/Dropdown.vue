<template>
  <div v-if="dropdownshow" class="dropdown">
    <ul>
      <li>
        <a href="#">
          <ProfileIcon />
          profile</a
        >
      </li>
      <li>
        <a href="#">
          <SignoutIcon />
          sign out</a
        >
      </li>

      <!-- when the size 699px -->
      <span class="links_in_699">
        <li>
          <a href="#">
            <PostsIcon />
            new post</a
          >
        </li>
        <li>
          <a href="#">
            <NotificationIcon />
            notifications</a
          >
        </li>
        <li>
          <a href="#">
            <WalletIcon />
            Wallet</a
          >
        </li>
      </span>
    </ul>
  </div>
</template>

<script>
import ProfileIcon from "./icons/ProfileIcon.vue";
import SignoutIcon from "./icons/SignoutIcon.vue";
import NotificationIcon from "./icons/NotificationIcon.vue";
import PostsIcon from "./icons/PostsIcon.vue";
import WalletIcon from "./icons/WalletIcon.vue";

export default {
  components: {
    ProfileIcon,
    SignoutIcon,
    PostsIcon,
    NotificationIcon,
    WalletIcon,
  },
  props: ["dropdownshow"],
};
</script>

<style scoped>
.dropdown {
  /* display: none; */
  position: absolute;
  color: white;
  top: 70px;
  right: 20px;
  z-index: 200;
  background-color: #333a44;
  width: 250px;
  border-radius: 10px;
}
ul li {
  list-style-type: none;
  /* background-color: rgb(65, 66, 65); */
  text-align: start;
  width: 90%;
  padding: 10px 0px;
  margin-bottom: 10px;
  border-radius: 10px;
}

ul li a {
  text-decoration: none;
  color: rgb(221, 218, 218);
  padding-left: 10px;
  text-transform: capitalize;
  display: flex;
  justify-content: start;
  align-items: center;
  gap: 5px;
}
ul li a svg {
  width: 20px;
  height: 20px;
}
ul li::before {
  content: "";
  border: 1px solid rgb(221, 218, 218);
  display: none;
}
ul li:hover {
  background-color: #4e576394;
}

.links_in_699 {
  display: none;
}

/* animation for the dropdown */
.dropdown {
  transform-origin: top center;
  animation: scaleZ 300ms ease-in-out forwards;
}
@keyframes scaleZ {
  0% {
    opacity: 0;
    transform: scale(0);
  }

  80% {
    transform: scale(1.07);
  }

  100% {
    opacity: 1;
    transform: scale(1);
  }
}


@media screen and (max-width: 699px) {
  .links_in_699 {
    display: block;
  }
}
</style>
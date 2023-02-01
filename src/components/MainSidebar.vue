<template>
  <div class="container">
  <div class="sidebar">
    <div>
      <router-link to="/" draggable="false"><img alt="logo" src="../assets/SpotifyLogo.png" width="130" height="40"/></router-link>
    </div>
    <div class="menu">
      <router-link to="/" class="submenu"><img alt="home-icon" :src="HomeIconSrc" width="24" height="24"><span>Home</span></router-link>
      <router-link to="/" class="submenu"><img alt="home-icon" src="../assets/SearchIconBlank.svg" width="24" height="24"><span>Search</span></router-link>
      <router-link to="/" class="submenu"><img alt="home-icon" src="../assets/LibraryIcon.svg" width="24" height="24"><span>Your Library</span></router-link>
    </div>
    <div class="menu">
      <router-link :to="{name: 'AboutView'}" class="submenu"><img alt="home-icon" src="../assets/CreatePlaylist.svg" width="24" height="24"><span>Create Playlist</span></router-link>
    </div>
    <div>Menu Item 1</div>
    <div>Menu Item 2</div>
    <div>Menu Item 3</div>
    <div>Menu Item 1</div>
    <div>Menu Item 2</div>
    <div>Menu Item 3</div>

  </div>
  </div>
</template>

<script>

  export default {
    data() {
      return {
      }
    },
    methods: {
    },
    computed: {
      HomeIconSrc() {
      if (this.$route.name === 'home') {
        return require('../assets/HomeIcon.svg')
      } else  {
        return require('../assets/HomeIconBlank.svg')
      }
    }
    }
  }
</script>

<style>
.container {
  height: 100%;
  width: 360px;
  position: fixed;
  top: 0;
  left: 0;
  padding-top: 30px;
  padding-left: 20px;
  background-color: black;
  color: darkgray;
}
.sidebar {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: flex-start;
  gap: 20px;
  font-weight: initial;
  height: 100%;
  font-size: 14px;
}

.menu {
  flex-grow: 0.12;
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: flex-start;
  gap: 13px;
  width: 160px;
  min-height: 10px;
}

.menu span {
  padding-left:20px;
  font-weight: 560;
}

.submenu {
  display:flex;
  flex-direction: row;
  align-items: center;
  flex-wrap: nowrap;
}

img, a {
  -webkit-user-drag: none;
}

a:link, a:visited {
    text-decoration: inherit;
    color: inherit;
    cursor: pointer;
}

/*
.sidebar {
display: grid;
grid-template-rows: 40% 60%;
gap: 2vh;
grid-auto-rows: 15px;
font-weight: initial;
height: 100%;
width: 26vw;
position: fixed;
top: 0;
left: 0;
padding-top: 30px;
padding-left: 20px;
background-color: black;
color: darkgray;
}

.sidebar .bottom {
  display: grid;
  grid-auto-rows: 2vh;
  text-align: left;
  gap: 1.5vh;
  font-size: 16px;
  overflow: scroll;
}


.sidebar .top {
  display: grid;
  grid-template-rows: 25% 45% 30%;
  grid-auto-rows: 2vh;
  text-align: left;
  gap: 1.5vh;
  font-size: 16px;
}
*/


</style>
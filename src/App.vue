<template>
  <div id="app">
    <mainTopbar />
    <MainSidebar />

  <router-view />
  </div>
</template>

<script>

import MainSidebar from './components/MainSidebar.vue'
import MainTopbar from './components/MainTopbar.vue'
  export default {
  name: 'App',
  components: { MainSidebar , MainTopbar },
  data() {
    return {
      colorGrad: '#1b1b1b'
    }
  },
  methods: {
  }
}
</script>

<style>
#app {
  font-family: 'CircularSp',sans-serif;
  font-size: 1.2rem;
  font-weight: 700;
  text-align: center;
  color: white;
  background: linear-gradient(180deg, v-bind(colorGrad) 0%, rgba(18,18,18,1) 40%);
  left: 0;
  top: 0;
  position: fixed;
  width: 100%;
  height: 100%;
}
a{
  color: white;
}
.footer {
  background-color: #181818;
}
*::-webkit-scrollbar {
  width: 16px;
}

*::-webkit-scrollbar-thumb {
  background: hsla(0,0%,100%,.3);
}

*::-webkit-scrollbar-button{
  display: none;
}
</style>

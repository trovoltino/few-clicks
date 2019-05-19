<template>
  <div id="app">
    <video autoplay muted loop id="myVideo">
      <source src="./assets/few-clicks-video.mp4" type="video/mp4">
    </video>
    <div class="shadow">
      <div class="main-content">
        <img src="./assets/FewClicks.png" alt="FewClicks" class="title-logo">
        <h3 class="info" v-bind:class="{ hide: show }">Making booklets and catalogs have never been easier!</h3>
      </div>
      <popup @hide-field = "hideField"/>
    </div>
  </div>
</template>

<script>

import popup from './components/pop-up.vue';

export default {
  name: 'app',
  components: {
    popup
  },
  methods: {
    hideField:function(value){
      this.show = value;
    }
  },
  data() {
    return{
      show: false
    }
  }
}
</script>

<style>
body{
  overflow: hidden;
  margin: 0px;
  padding: 0px;
}
#myVideo {
  position: fixed;
  top: 50%;
  left: 50%;
  min-width: 100%; 
  min-height: 100%;
  z-index: -1;
  transform: scale(1.4, 1.4) translate(-36%, -36%);

}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f6f6f6;
  height: 100vh;
}
.shadow {
  background:rgba(0, 0, 0, 0.5);
  z-index: 10;
  height: 100vh;
}
h3 {
  font-size: 1.5em;
  text-transform: uppercase;
  
}
.title-logo{
  height: 450px;
  background: transparent;
}
.main-content{
  width: 90%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -80%);
  display: flex;
  flex-direction: column;
  align-items: center;
}
.hide{
  visibility: hidden;
}

</style>

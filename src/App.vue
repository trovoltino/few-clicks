<template>
  <div id="app">
    <div class="shadow">
      <HelloWorld class="main-content" msg="FewClicks"/>
      <popup/>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import popup from './components/pop-up.vue';

export default {
  name: 'app',
  components: {
    HelloWorld,
    popup
  }
}
</script>

<style>
body{
  overflow: hidden;
  margin: 0px;
  padding: 0px;
}
#app {
  background: url(./assets/FewLogo.jpg) no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f6f6f6;
  height: 100vh;
  
 
}
.logo-container {
  width: 100%;
  height: auto;
  margin: 0px;
  padding: 0px;
}
.main-content {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -75%);

}
.shadow {
  background:rgba(0, 0, 0, 0.7);
  z-index: 100;
  height: 100vh;
  
}

</style>

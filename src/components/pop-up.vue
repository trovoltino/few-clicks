<template>
  <div class="container" v-on:click="show=!show" v-bind:class="{ hide: show }">
    <form action="" v-bind:class="{ formShow: show }">
      <input type="text" placeholder="Name">
      <input type="email" name="email" id="email" placeholder="email">
      <textarea name="message" rows="10" cols="30">
          The cat was playing in the garden.
      </textarea>
      <input type="button" value="submit">
    </form>
    <p class="contact">contact us</p>
  </div>
</template>

<script>
export default {
  name: 'pop-up',
  data() {
    return{
      show: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .container {
    position: absolute;
    bottom: 0px;
    left: 50%;
    transform: translate(-50%, 50%);
    height: 150px;
    width: 320px;
    -moz-border-radius: 150px / 80px;
    -webkit-border-radius: 150px / 80px;
    border-radius: 150px / 80px;
    background:rgb(63, 63, 63);
    transition: all 1s ease-in-out;
    border: solid black 1px;
    box-shadow: 2px silver;
  }
  
  p {
    text-align: center;
    text-transform: uppercase;
    font-size: 20px;
    font-weight: 600;
    color: white;
    position: relative;
    bottom: 0px;
    top: 0%;
    width: 100%;
    text-transform: uppercase;
  }
  form {
    display: none;
    transition: all 1s ease-in-out;
  }
  .formShow {
    display: flex;
    flex-direction: column;
    
  }
  .hide {
    height: 75%;
    width: 45%;
  }
</style>
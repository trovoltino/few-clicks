<template>
  <div class="container">
    <form action="">
      <input type="text" placeholder="Name">
      <input type="email" name="email" id="email" placeholder="email">
      <input type="button" value="submit">
    </form>
    <p class="contact">contact us</p>
  </div>
</template>

<script>
export default {
  name: 'pop-up'
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
    background: rgb(196, 50, 50);
    transition: all 1s ease-in-out;
  }
  .container:active {
    height: 75%;
    width: 45%;
    
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
  }
</style>
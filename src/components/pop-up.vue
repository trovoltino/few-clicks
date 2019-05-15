<template>
  <div class="container" v-on:click="show=!show" v-bind:class="{ containerShow: show }">
    <form action="" v-bind:class="{ formShow: show }">
      <input type="text" placeholder="Name">
      <input type="email" name="email" id="email" placeholder="email">
      <textarea name="message" rows="10" cols="30">
          The cat was playing in the garden.
      </textarea>
      <button>submit</button>
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
    border-radius: 70px;
    background:rgba(48, 48, 48, 0.8);
    transition: all 1s ease-in-out;
    border: solid black 1px;
    box-shadow:inset 0px 0px 0px 1px #bee2f9;
    border:1px solid #b4b4b4;
    cursor:pointer;
    color:#14396a;
    text-shadow:0px 1px 0px #dee0e2;
  }
  .btn-look {
    box-shadow:inset 0px 0px 0px 1px #bee2f9;
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
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-105%);
    width: 70%;
  }
  form input, form textarea{
    color: white;
    border: white solid 2px;
    border-radius: 10px;
    background: transparent;
    position: relative;
    left: 50%;
    transform: translate(-50%,0%);
  }
  button {
    padding: 10px;
    border-radius: 20px;
    cursor: pointer;
    margin: 10px 0px;
    text-transform: uppercase;
    font-weight: 700;
    font-family: sans-serif;
  }
  input {
    height: 30px;
    text-align: center;
    margin: 10px 0px;
  }
  textarea {
    margin: 10px 0px;
  }
  .formShow {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
  .containerShow {
    height: 850px;
    width: 650px;
  }
  .hide {
    display: none;
  }
</style>
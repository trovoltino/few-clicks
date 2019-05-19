<template>
  <div class="container" v-bind:class="{ containerShow: !show }">
    <div class="slide-up" @click="handler()">
      <img class="slide-up-first" src="../assets/up-chevron.svg" alt="" v-bind:class="{ invisible: !show }">
      <img class="slide-up-second" src="../assets/up-chevron.svg" alt="" v-bind:class="{ invisible: !show }">
    </div>
    
    <form action="" v-bind:class="{ formShow: show }">
      <input type="text" placeholder="Name">
      <input type="email" name="email" id="email" placeholder="email">
      <textarea name="message" rows="10" cols="30">
          The cat was playing in the garden.
      </textarea>
      <button>submit</button>
    </form>
    <p v-bind:class="{ hide: show }" class="contact">contact us</p>
  </div>
</template>

<script>

export default {
  name: 'pop-up',
  data() {
    return{
      show: true
    }
  },
  methods: {
    showForm:function(){
      this.show = !this.show;
      
    },
    hideParentFields:function(){
      this.$emit('hide-field', this.show);
    },
    handler:function() {
      this.showForm();
      this.hideParentFields();
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
    height: 1050px;
    width: 850px;
    border-radius: 70px;
    background:rgba(48, 48, 48, 0.8);
    transition: width, height, 1s ease-in-out;
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
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    text-align: center;
    text-transform: uppercase;
    font-size: 24px;
    font-weight: 600;
    color: white;
    position: relative;
    top: -55%;
    width: 100%;
    text-transform: uppercase;
    z-index: -1;
  }
  .slide-up-first, .slide-up-second{
    height: 40px;
    color:white;
    transform: rotateX(180deg);
  }
  .slide-up-first {
    margin-top: 10px;
    margin-bottom: -25px;
  }
  .slide-up {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    padding-bottom: 10px;
  }
  form {
    display: none;
    transition: width, height, 1s ease-in-out;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-140%);
    width: 70%;
  }
  form input, form textarea{
    color: white;
    box-shadow:inset 0px 0px 0px 1px #bee2f9;
    border:1px solid #b4b4b4;
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
    /* height: 1050px;
    width: 850px; */
    height: 150px;
    width: 420px;
  }
  .containerShow:hover {
    background: #656566;
  }
  .hide {
    display: none;
  }
  .invisible {
    visibility: hidden;
  }
  .red {
    color: red;
  }
</style>
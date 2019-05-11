<template>
  <div class="main">
    <div class="hello">
      <img src="../assets/FewCliks.png" alt="FewClicks" class="title-logo">
      <h1>{{ msg }}</h1>
    </div>
    <h3 class="info">Making booklets and catalogs have never been easier!</h3>
    <button class="contact" type="button">contact us</button>
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.hello {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0px;
  padding: 0px;
}
.title-logo{
  height: 130px;
}
h1 {
  font-size: 8em;
  font-family: auto;
  margin: 0px 0.5em;
}
h3 {
  font-size: 1.5em;
  text-transform: uppercase;
}
.contact {
  padding: 10px 20px;
  font-size: 20px;
  border-radius: 60%;
}
</style>

<template>
  <div class="home">
    <HelloWorld msg="Se connecter"/>

    <div id="connection">

      <div></div>

      <form action="" method="post">
        <img src="../assets/user.svg" id="user" alt="">
        <input type="text" placeholder="Pseudo Admin" id="input">
        <br><br>
        <input type="password" name="" placeholder="Mot de passe" id="input">
        <br><br>
        <button type="submit" id="soumettre"> Soumettre </button>
      </form>

      <div></div>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
  .home
  {
    position: relative;
    align-self: center;
  }
  #connection
  {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
  }
  form
  {
    padding: 100px;
    background-color: #1787ff;
    border: 1px solid transparent;
    box-shadow: 0px 0px 30px gray;
  }
  form #user
  {
    max-height: 100px;
    padding-bottom: 30px;
  }
  #input
  {
    margin: auto;
    width: 100%;
    padding: 10px;
    display: block;
    border: 2px solid transparent;
  }
  #input:hover, #input:focus, #input:active
  {
    border-color: green;
  }
  #soumettre
  {
    padding: 10px;
    background-color: green;
    font-weight: bold;
    color: white;
    border: 2px solid black;
    transition-property: all;
    transition-duration: 300ms;
  }
  #soumettre:hover
  {
    background-color: rgb(3, 168, 3);
  }
</style>

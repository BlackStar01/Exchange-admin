<template>
  <div id="app">
    <div id="nav">

      <div id="logo">
        <img src="../src/assets/logo.png" alt="">
      </div>

      <router-link to="/">Home</router-link>
      <router-link v-if="estAdmin" to="/e-change">E-change</router-link>
      <router-link v-if="estAdmin" to="/traduction">Traduction</router-link>
      <router-link v-if="estAdmin" to="/transcription">Transcription</router-link>
      
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      estAdmin: true,
    }
  },
}
</script>

<style>

:root {
  --blue: #39A7F6;
  --transparent: rgba(255, 255, 255, 0);
  --bluehover: #1787ff;
  --vert: #00973A;
}
 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 4fr;
}

#nav {
  height: 97vh;
  box-shadow: 0px 10px 20px grey;
}

#nav #logo {
  padding-top: 20%;
  padding-bottom: 20%;
}

#nav #logo img {
  max-height: 100px;
}

#nav a {
  font-weight: bold;
  display: block;
  padding: 8%;
  color: black;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: var(--vert);
}
</style>

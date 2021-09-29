<template>
  <div class="e-change">
    <h1> Reserves de devises </h1>
    <hr>

    <div id="reserves">
      <div id="stock" v-for="devise in devises" :key="devise.id">
          <div class="stock">
            <h3> {{ devise.name }}</h3>
            <h1> {{ devise.restant }} </h1>
          </div>
      </div>
    </div>

    <div id="others">

      <div>
        <h1> Recharger </h1>
        <hr>
          <br><br>
        <form action="" method="post">
          <select id="select" name="">
            <option v-for="devise in devises" v-bind:key="devise.id"> {{devise.name}} </option>
          </select>
          <br><br>
          <button type="submit" id="submit"> Reharger </button>
        </form>
      </div>

      <div>
        
      </div>

    </div>

    
  </div>
</template>

<script>
export default {
  data() {
    return {
      devises : [
        {
          id: 1,
          name: 'XOF',
          restant: 15369000
        },
        {
          id: 2,
          name: '$',
          restant: 5000
        },
        {
          id: 3,
          name: '£',
          restant: 17000
        }
      ]
    }
  },

}
</script>

<style scoped>
:root {
  --blue: #39A7F6;
  --transparent: rgba(255, 255, 255, 0);
  --bluehover: #1787ff;
  --vert: #00973A;
}

#reserves {
  display: flex;
  width: 95%;
  margin: auto;
}
#stock {
  border: 1px solid black;
  box-shadow: 0px 0px 30px #ccc;
  width: 25%;
  margin: 5%;
  overflow: hidden;
  position: relative;
  align-self: center;
}
.stock
{
  background-color: var(--blue);
  padding-top: 10%;
  padding-bottom: 10%;
}
#others
{
  display: grid;
  grid-template-columns: 1fr 1fr;
}
#select
{
  width: 90%;
  padding: 2%;
}
#submit
{
  width: 90%;
  background-color: var(--vert);
  padding: 2%;
  border: 1px solid black;
  transition-duration: 500ms;
  transition-property: all;
}
#submit:hover
{
  background-color: var(--blue);
}
  
</style>
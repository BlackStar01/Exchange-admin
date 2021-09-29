<template>
  <div class="e-change">
    <h1> Reserves de devises </h1>
    <hr>

    <div id="reserves">
      <div id="stock">
          <div class="stock">
            <h3> Traductions demandées </h3>
            <h1> {{ demandes }} </h1>
          </div>
      </div>
      <div id="stock">
          <div class="stock">
            <h3> Traductions effectuées </h3>
            <h1> {{ fini }} </h1>
          </div>
      </div>
    </div>

    <div id="others">

      <div>
        <h1> Demandes de traductions </h1>
        <hr>
        <br><br>
        <table class="table">
            <thead>
                <tr>
                    <th> Fichier à traduire </th>
                    <th> Adresse de l'expéditeur </th>
                </tr>
            </thead>
            <tbody>

                <!-- UN VFOR SERAIT ADEQUAT -->
                <tr id="tr">
                    <td>
                        <!--    Le fichier qui a été envoyé     -->
                        <a href="" download=""> Télécharger </a>
                    </td>
                    <td>
                        <p> ncifc@uefchuf.dd</p>
                    </td>
                </tr>
            </tbody>
        </table>
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
        demandes: 0,
        fini: 0,
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
th
{
    padding: 15px;
    border: 1px solid black;
}
  
</style>
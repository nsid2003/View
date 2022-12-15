<template>
  <div class="about">
    <h1>FORMULAIRE 2</h1>
    <br/>
    <br/>
    <div class="formualire">
      <br/>
      <p>
        <form>

        </form>
          <label> Unité à convertir </label> <input type="text" v-model="valeurdepart">
          <select v-model="unitedepart">
            <option value="Metre">Metre</option>
          </select>
          <br/>
          <br/>
          <label> Resultat </label> <input type="text" v-model="resultat">
          <select v-model="unitearrive">
            <option value="Centimetre">Centimetre</option>
          </select>
          <br/>
          <br/>
          <button @click="convertir"> Convertir </button>
          <br/>
          <br/>
        {{ phrase }}
      </p>
        
    </div>
  </div>
 
</template>

<script lang="ts">
  export default {

    data(){
      return {
        msg : "bonjour",
        valeurdepart:0,
        phrase :"",
        resultat:0,
        unitedepart:"",
        unitearrive:"",

        
      }
    },
    methods:{
      ajouter(){
        this.phrase = "je m'appelle " + this.nom + this.prenom;
      },
      convertir(){
      if(this.unitedepart== "Metre" && this.unitearrive =="Centimetre") 
      {
        this.resultat = this.valeurdepart * 100;
      }
    }
    
    }
  }
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<template>
  <div class="about">
    <h1>CONVERTISEUR DE DEVISE</h1>
    <br/>
    <br/>
    <div class="formualire">
      <br/>
      <p>
        <form>

        </form>
          <label> Unité à convertir </label> <input type="text" v-model="valeurdepart">
          <select v-model="unitedepart">
            <option value="XAF">XAF</option>
            <option value="EUR">EUR</option>
            <option value="USD">USD</option>
            <option value="GBP">GBP</option>
          </select>
          <br/>
          <br/>
          <label> Resultat </label> <input type="text" v-model="resultat">
          <select v-model="unitearrive">
            <option value="XAF">XAF</option>
            <option value="EUR">EUR</option>
            <option value="USD">USD</option>
            <option value="GBP">GBP</option>
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
        this.phrase = " Conversion réussie !"
      },
      convertir(){
      if(this.unitedepart== "XAF" && this.unitearrive =="EUR") 
      {
        this.resultat = this.valeurdepart * 650;
      }
      if(this.unitedepart== "XAF" && this.unitearrive =="USD") 
      {
        this.resultat = this.valeurdepart * 630;
      }
      if(this.unitedepart== "XAF" && this.unitearrive =="GBP") 
      {
        this.resultat = this.valeurdepart * 1000;
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
  
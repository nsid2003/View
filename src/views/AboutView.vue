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
          <label> Nom </label> <input type="text" v-model="nom">
          <br/>
          <br/>
          <label> prenom </label> <input type="text" v-model="prenom ">
          <br/>
          <br/>
          <button @click="ajouter">Faire la phrase</button>
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
        nom : "",
        prenom :"",
        phrase :""

        
      }
    },
    methods:{
      ajouter(){
        this.phrase = "je m'appelle" + this.nom + this.prenom;
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

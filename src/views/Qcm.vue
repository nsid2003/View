<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div class="about">
    <h1>Quiz [ score {{ score }}/2]</h1>
    <br />
    <h3>{{ questions[index].question }}</h3>
    <p v-for="item in questions[index].reponses"> 
      {{ item }}
    </p>
    <input type="text" v-model="proposition" />
    <P>
      <button @click="valider">Valider</button>
      <button @click="suivant(index)">Suivant</button>
      <button @click="precedent(index)">precedent</button>
    </P>
  </div>
</template>

<script lang="ts">
// declaration des variables et des methodes
export default {
  data() {
    // delclaration des variables
    return {
      index: 0,
      score: 0,
      proposition: 0,
      questions: [
        {
          question: "Quelle est la capitale du Cameroun?",
          reponses: ["Douala", "Yaoundé", "Buea"], // tableaux des reponses 
          ok: 1,
        },
        {
          question: "Dans quelle region est la capitale du Cameroun?",
          reponses: ["Littoral", "Centre", "Nord"], // tableau des reponses
          ok: 1,
        },
      ],
    };
  },
  methods: {
    suivant() {
      this.index++; // permet d'aller a la question suivante
    },
    precedent() {
      this.index--; // permet de revenir à la question précédente
    },
    valider() {
      if (this.proposition == this.questions[this.index].ok) {
        // permet de valider la reponse
        this.score++;
      }
    },
  },
};
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: block;
    align-items: center;
  }
}
</style>

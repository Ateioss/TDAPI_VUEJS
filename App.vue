<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

import Cour from "./components/Cour.vue";

</script>

<template>
  <div style="border:1px #0f6674 solid;background-color:#0f6674;
               border-bottom:2px white solid;padding:20px;
               font-size:28px;">
    <h1 style="color:white;">Liste de cours</h1>
  </div>
  <div style="display:flex; flex-direction:row; justify-content:center;gap:20px;flex-wrap:wrap;">

  <Cour v-for="cour in listecours"
      :nom="cour.nom"
      :description="cour.description"
      :programme="cour.programme"
      :year="cour.year"
      :date_debut="cour.date_debut"
      :date_fin="cour.date_fin"
      :image_url="cour.image_url"
    />


  </div>
</template>

<style scoped>

</style>

<script>

const url = 'http://localhost:8000/api/cours';

const options = {
  method : 'GET',
  headers:{
    'Accept':'application/json',
    'Content-type':'application/json',
  }
}

async function getCours() {
  try {
    let res = await fetch(url,options);
    return await res.json();
  } catch (error) {
    console.log(error);
  }
}

const listecours = await getCours();

export default {
  setup() {
    return {
      listecours
    }
  }
}
</script>
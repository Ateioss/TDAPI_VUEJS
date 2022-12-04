<script setup>
defineProps(['nom', 'programme', 'description', 'year', 'date_debut', 'date_fin', 'image_url'])
</script>

<template>
  <div class="card">
    <div class="card-img">
      <img style="width:100%;" src="{{image_url}}">
    </div>
    <div class="card-group-infos">
      <div class="card-infos">
        <p class="card-info">Nom</p>
        <p class="card-info2">{{nom}}</p>
      </div>
      <div class="card-infos2">
        <p class="card-info">Description</p>
        <p class="card-info2">{{description}}</p>
      </div>
      <div class="card-infos">
        <p class="card-info">Programme</p>
        <p class="card-info2">{{programme}}</p>
      </div>
      <div class="card-infos2">
        <p class="card-info">Year</p>
        <p class="card-info2">{{year}}</p>
      </div>
      <div class="card-infos">
        <p class="card-info">Date debut</p>
        <p class="card-info2">{{date_debut}}</p>
      </div>
      <div class="card-infos2">
        <p class="card-info">Date fin</p>
        <p class="card-info2">{{date_fin}}</p>
      </div>
    </div>
  </div>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}

.card{
  background-color:#0f6674;
  width:20%;
  margin-top:20px;
}
.card-img{
  padding:10px;
  padding-bottom:0px;
}
.card-group-infos{
  padding:10px;
}
.card-infos{
  background-color:#9fcdff;
  padding:10px;
  display:flex;
  flex-direction:row;
}
.card-infos2{
  background-color: #7da0b1;
  padding:10px;
  display:flex;
  flex-direction:row;
}
.card-info{
  color:white;
  font-weight:bold;
  width: 40%;
}
.card-info2{
  color:white;
  text-align: center;
}
</style>
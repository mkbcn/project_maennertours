<template>
  <div class="card text-bg-dark mb-3" style="width: 23rem;">
 
  <div class="card-header">
    Youtube Video
  </div>
  <iframe width="366" height="175" src="https://www.youtube.com/embed/GQaWi69s-MI?si=LFyIpFct_-a9L4Iq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  <!--<img src="../assets/trailerStill.png" class="card-img-top" alt="maenner foto">-->
  <div class="card-body">
    <h5 class="card-title">{{ title }}</h5>
    <p class="card-text">{{ text }}</p>
    <a href="#" class="btn btn-primary">{{ btntext }}</a>
  </div>
</div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  title: String,
  text: String,
  btntext: String,
  btnlink: String
});
</script>

<style scoped>
.card{
  border-radius: 10px;
  border: 1px solid #727272;
  
  margin-top: 80px;;
}
</style>
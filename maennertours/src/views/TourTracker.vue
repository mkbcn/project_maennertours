<script setup>
import { useI18n } from 'vue-i18n';
import { ref, watch } from 'vue';


const { t, locale } = useI18n();
const instaText = ref(t('message.instaText'));

// Watch the locale and update the translated message and video title whenever it changes
watch(locale, () => {

  
    instaText.value = t('message.instaText');
});
</script>

<template>
  <div class="bg-image rounded-3">
    <div class="container-fluid">
      <div class="row" >
        <div class="col-lg-2"></div>
        <div class="col-lg-4" >
          <div class="fs-4">
            {{ instaText }}
          </div>
        </div>
        <div class="col-lg-1"></div>
        <div class="col-lg-4">
         
            <iframe src="https://maennertours.autoskope.de/"></iframe>        
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bg-image
{
  background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), 
                    url(../assets/alpenWechsel.png);
  background-size: cover;
  background-position: center;
  height: 80vh;
  position: relative;
  border: 1px solid #727272;
}
.row {
  color: #c0c0c0;
  z-index: 1000;
  padding-top: 6%;
}
.fs-4 {
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 10px 80px 10px 80px;
  padding: 40px;
  text-align: center;
  border: 1px solid #727272;
}
.list-group{
    max-height: 450px;
    margin-bottom: 10px;
    overflow:scroll;
    -webkit-overflow-scrolling: touch;
}
.list-group-item{
  background-color: #272626e6;
  align-self: auto;
}
.instagram-frame {
  scrollbar-width: none;
  -ms-overflow-style: none;
  overflow: hidden;
  border: none;
  border-radius:10px;
}

.instagram-frame::-webkit-scrollbar {
  display: none;
}
</style>

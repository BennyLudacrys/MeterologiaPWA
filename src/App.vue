<template>
<weather />

</template>
<script >
import Weather from './components/Weather.vue';
export default{
  name: 'app',
  components: {
    Weather,
  }
};

</script>

<style>

 body {
  overflow-y: hidden;
  height: 100vh;
  background: rgb(65, 21, 48);
  background: linear-gradient(
    -185deg,
    rgba(65, 21, 48, 1) 55%,
    rgba(255, 255, 255, 1) 55%
  );
} 

@media only screen and (min-width: 360px) and (max-width: 908px) {
  body {
    overflow-y: auto;
  }
}


</style>





 




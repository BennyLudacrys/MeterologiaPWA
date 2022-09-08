<template>
  <div class="card">
    <div class="card-body">
      <h2 class="card-title" v-if="dados">{{ dados[0] }}</h2>
      <div id="sun">
        <img
          v-if="dados[3] == 'Rain'"
          src="../assets/heavy-rain (1).png"
        />
        <img
          v-if="dados[3] == 'Clouds'"
          src="../assets/clouds.png"
        />
        <img
          v-if="dados[3] == 'Clear'"
          src="../assets/contrast.png"
        />
      </div>
      <div id="graus">
        <h4><span>Min: </span>{{ dados[1]-2 }}&deg;</h4>
        <h4><span>Max: </span> {{ dados[2] }}&deg;</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["dados"],
};
</script>

<style scoped>
#sun {
  display: flex;
  justify-content: center;
  height: 100px;
}

.card {
  width: 18rem;
  height: 200px;
  margin-top: 100px;
  background: #5e6f7a;
  color: rgb(7, 7, 7);
  border-radius: 10%;
}

h2 {
  text-align: center;
}

h4 {
  font-size: 15px;
}

h4 span {
  font-size: 23px;
  color: rgb(14, 22, 139);
}

#graus {
  margin-top: 30px;
  font-style: italic;
  display: flex;
  width: 100%;
  justify-content: space-between;
}


</style>
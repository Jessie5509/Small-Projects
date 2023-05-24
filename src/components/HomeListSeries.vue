<template>
  <div class="container">
    <div v-for="serie in series" :key="serie.id">
      <div class="series-container">
        <img :src=serie.img alt="" style="width: 145px; height: 200px;">
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      series: [
        { name: "Orphan Black", id: 1, details: "Hola", img: require('../assets/004_p.jpg') },
        { name: "Warrior Nun", id: 2, details: "Hola", img: require('../assets/dest_3.jpg') },
        { name: "Wynonna Earp", id: 3, details: "Hola", img: require('../assets/001_p.jpg') },
        { name: "Orange is the new black", id: 4, details: "Hola", img: require('../assets/a.jpg') },
        { name: "Dark", id: 5, details: "Hola", img: require('../assets/Dark_Poster.jpg') },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: 5px;
}

.series-container {
  width: 145px;
  height: 200px;
  margin: 7px;
}
</style>

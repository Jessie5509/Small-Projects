<template>
  <div class="list-container">
    <h1>My list</h1>
    <GlobalButton v-for="item in btnList" :key="item.id" :text="item.name" @toggle-btn="toggleBtn" />
    <div class="card-container">
      <div v-for="l in list" :key="l.id" class="card">
        <img :src="l.img" alt="" style="width: 145px; height: 200px;">
      </div>
    </div>
  </div>
</template>

<script>
import GlobalButton from "../components/GlobalButton.vue";
export default {
  data() {
    return {
      btnList: [
        { name: 'Books', id: 1 },
        { name: 'Series', id: 2 },
        { name: 'Anime', id: 3 },
        { name: 'Manga', id: 4 },
      ],
      list: [],
      books: [
        { name: 'Neuromancer', id: 5, img: require('../assets/neuro.jpg') },
        { name: 'Chicas de tormentas y sombras', id: 6, img: require('../assets/chicas.jpg') },
        { name: 'Volviendo al amor', id: 7, img: require('../assets/amor.jpg') },
        { name: 'Night Owls And Summer Skies', id: 8, img: require('../assets/nightowls.jpg') },
        { name: 'Her name in the sky', id: 9, img: require('../assets/hername.jpg') }
      ],
      series: [
        { name: "Orphan Black", id: 10, details: "Hola", img: require('../assets/004_p.jpg') },
        { name: "Warrior Nun", id: 11, details: "Hola", img: require('../assets/dest_3.jpg') },
        { name: "Wynonna Earp", id: 12, details: "Hola", img: require('../assets/001_p.jpg') },
        { name: "Orange is the new black", id: 13, details: "Hola", img: require('../assets/a.jpg') },
        { name: "Dark", id: 14, details: "Hola", img: require('../assets/Dark_Poster.jpg') },
      ],
      anime: [
        { name: 'Cyberpunk', id: 15, img: require('../assets/cyber.jpg') },
        { name: 'Naruto', id: 16, img: require('../assets/naruto.jpg') },
        { name: 'Dragon ball', id: 17, img: require('../assets/dragonball.jpg') },
        { name: 'Kakegurui', id: 18, img: require('../assets/Kakegurui.jpg') },
        { name: 'Birdie wing', id: 19, img: require('../assets/Birdie.jpg') },
        { name: 'Citrus', id: 20, img: require('../assets/Citrus.jpg') }
      ],
      manga: [
        { name: 'Lily S2', id: 21, img: require('../assets/lily.jpg') },
        { name: 'Getting to know Grace', id: 22, img: require('../assets/grace.jpg') },
        { name: 'Sadistic Beauty', id: 23, img: require('../assets/sadistic.jpg') },
        { name: 'Shitsurakuen', id: 24, img: require('../assets/shitsurakuen.jpg') }
      ],
    }
  },
  components: {
    GlobalButton,
  },
  methods: {
    toggleBtn(text) {
      this.showList = !this.showList;
      this.getList(text);
    },
    getList(text) {
      switch (text) {
        case 'Books':
          this.list = this.books;
          break;
        case 'Series':
          this.list = this.series;
          break;
        case 'Anime':
          this.list = this.anime;
          break;
        case 'Manga':
          this.list = this.manga;
          break;
        default:
          break;
      }
    }
  }

}
</script>

<style scoped>
.list-container {
  display: inline-block;
  width: 55%;
  height: inherit;
  margin-top: 40px;
  border: solid;
  background-color: darkgrey;
}

.card-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.card {
  margin-right: 10px;
  margin-top: 30px;
}
</style>
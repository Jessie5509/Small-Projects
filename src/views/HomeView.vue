<template>
  <div class="home">
    <HomeListSeries />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import HomeListSeries from "../components/HomeListSeries.vue";

@Options({
  components: {
    HomeListSeries,
  },
})
export default class HomeView extends Vue { }
</script>

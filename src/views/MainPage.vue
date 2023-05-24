<template>
  <div class="main-container">
    <nav class="main-nav">
      <router-link :to="{ name: 'home' }" class="router">Home</router-link>
      <router-link :to="{ name: 'list' }" class="router">List</router-link>
      <div class="profile">
        <img src="../assets/p.jpg" alt="" style="width: 45px; height: 45px;">
      </div>
    </nav>

    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.main-nav {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
  height: 55px;
  border-radius: 5px;
  background-color: grey;
}

.main-container {
  width: 100%;
  height: 800px;
  background-color: rgb(26, 26, 29);
}

.router {
  margin: 0px 20px 0px 0px;
  text-decoration: none;

}

.profile {
  margin: 0px 15px 0px 0px;
  align-items: center;
}
</style>

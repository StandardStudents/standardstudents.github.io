<template>
  <div>
    <a href="https://github.com/StandardStudents/" target="_blank">
      <img id="logo" src="../assets/logo.png" alt="The Standard Students Logo" :width="dim" :height="dim">
    </a>
    <h1 id="title"><router-link id="title-link" :to="{ name: 'Lander' }">The Standard Students Podcast</router-link></h1>
    <p>Check us out on <a target="_blank" href="https://itunes.apple.com/us/podcast/standard-students-podcast/id1273635244?mt=2">iTunes!</a></p>
    <div class="menu">
      <router-link :to="{ name: '', params: {} }">Blog</router-link>
      <router-link :to="{ name: 'Archive'}">Archive</router-link>
      <router-link :to="{ name: 'About'}">About</router-link>
    </div>
  </div>
</template>

<script>
export default {
  props: ['dim'] // image dimensions
}
</script>

<style media="screen" scoped>
@import "../assets/main.css";
h1 {
  text-decoration: none;
  font-weight: normal;
  text-align: center;
  color: #000;
}
#title-link {
  color: #000;
  text-decoration: none;
}
p {
  text-align: center;
  font-size: 20px;
}
.menu {
  display: flex;
  justify-content: space-around;
}
.menu-item {
  font-size: 20px;
}
#logo {
  display: block;
  margin: auto;
}
</style>

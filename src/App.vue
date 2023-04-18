<template>
  <nav>
    <router-link to="/">Home</router-link>
  </nav>
  <router-view/>
  <div class="model">
    <Spline :scene="scene" />
  </div>
</template>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

.model{
  width: 100vw;
  height: 100vh;
  position: absolute;
  top: 0;
  left: 0;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import { defineComponent } from 'vue';
import Spline from "spline-vue/v3";

export default defineComponent({
  name: 'App',
  components: {
    Spline
  },
  data: () => ({
    scene: "https://prod.spline.design/2XVCWOkcGNZH0hue/scene.splinecode",
  })
});
</script>
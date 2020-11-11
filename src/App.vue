<template>
  <WhatsMyIp/>
</template>

<script>
import WhatsMyIp from './components/WhatsMyIp.vue'

export default {
  name: 'App',
  components: {
    WhatsMyIp
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
body{
  margin: 0;
  padding: 0;
  position: absolute;
  height: 100%;
  width: 100%;

}
#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  flex-direction: row;
}
</style>

<template>

  <HeaderComponent />
  <PortfolioPedro />
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.15.1/devicon.min.css">

</template>

<script>
import PortfolioPedro from '@/components/Portfolio.vue';
import HeaderComponent from './components/Header.vue';

export default {
  name: 'App',
  components: {
    PortfolioPedro,
    HeaderComponent
  }
}
</script>

<style>
@font-face {
  font-family: Ubuntu-regular;
  src: url(@/assets/font/ubuntu/Ubuntu-R.ttf);
}

html{
  scroll-behavior: smooth;
}

body {
  background-color: black;
  margin: 0 !important;
  padding: 0 !important;
}

#app {
  font-family: Ubuntu-Regular;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #e8e8e8;
}
</style>

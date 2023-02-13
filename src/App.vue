<template>
  <HeaderComponent />
  <PortfolioPedro />
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.15.1/devicon.min.css">
  <FooterComponent />
</template>

<script>
import PortfolioPedro from '@/components/Portfolio.vue';
import HeaderComponent from './components/Header.vue';
import FooterComponent from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    PortfolioPedro,
    HeaderComponent,
    FooterComponent
  }
}
</script>

<style>
@font-face {
  font-family: Ubuntu-regular;
  src: url(@/assets/font/ubuntu/Ubuntu-R.ttf);
}

html {
  scroll-behavior: smooth;
}

body {
  background-color: rgb(23, 23, 23);
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

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #2e2e2e;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #fff;
  border-radius: 5px;

}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #ccc;
}
</style>

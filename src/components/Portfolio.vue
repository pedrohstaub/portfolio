<template>
  <div class="content">
    <div id="about">
      <hr>
      <h1>Quem sou eu?</h1>
      <h3>
        Meu nome é Pedro, sou desenvolvedor web desde 2019.
      </h3>
      <h3 style="text-align:center">
        Trabalho com desenvolvimento web desde 2019, fornecendo softwares para empresas de
        segurança privada e monitoramento. As soluções que construí junto com minha equipe impactam
        diariamente mais de <i>100.000</i> usuários no mundo inteiro. <br /><br />
        Procuro oportunidades onde possa exercer minha experiência adquirida durante esses
        anos e estou sempre disposto a aprender e superar novos desafios.
      </h3>
      <br />
      <hr>
    </div>
    <div id="tech">
      <h1>
        Tecnologias
      </h1>
      <div class="tech" align="center">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-plain-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-plain-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg" />
      </div>
      <br />
      <hr>
    </div>
    <div id="projects">
      <h1>
        Projetos
      </h1>
      <card-projects :titleCard="p1Name" :text="p1Text"></card-projects>
    </div>
  </div>
</template>

<script>
import CardProjects from './CardProjects.vue';

export default {
  name: 'PortfolioPedro',
  data() {
    return {
      p1Name: 'Site IBNA',
      p1Text: 'Site criado para a IBNA SCS, feito em PHP e JS e Bootstrap utilizando o tema Assan.'
    }
  },
  props: {
    msg: String
  },
  components: {
    CardProjects
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

hr {
  border: none;
  height: 1px;
  background-color: #ffffffa7
}

.tech>img {
  width: 10%;
  margin: 2%;
}

.tech>img:hover {
  animation: tech-animate 200ms;
  animation-fill-mode: forwards;
}

.content {
  margin: 7%;
}

@keyframes tech-animate {
  0% {
    width: 10%;
  }

  25% {
    width: 10.3%;

  }

  50% {
    width: 10.5%;
  }

  75% {
    width: 10.9%;
  }

  100% {
    width: 11.2%;
  }
}
</style>

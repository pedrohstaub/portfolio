<template>
  <div class="content">
    <div id="about">
      <hr>
      <h1>Quem sou eu?</h1>
      <h3>
        Meu nome é Pedro tenho {{ age }} anos, sou desenvolvedor web fullstack.
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
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-plain-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original-wordmark.svg" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-plain-wordmark.svg" />

      </div>
      <br />
      <hr>
    </div>
    <div id="projects">
      <h1>
        Projetos
      </h1>
      <br />
      <div class="projects">
        <card-projects :titleCard="ibnaName" :text="ibnaText" :img="ibnaImg" :link="ibnaLink"></card-projects>
        <card-projects :titleCard="solutioName" :text="solutioText" :img="solutioImg"
          :link="solutioLink"></card-projects>
        <card-projects :titleCard="dayzName" :text="dayzText" :img="dayzImg" :link="dayzLink"></card-projects>
        <card-projects :titleCard="portfolioName" :text="portfolioText" :img="portfolioImg"
          :link="portfolioLink"></card-projects>
      </div>
    </div>
  </div>
</template>

<script>
import CardProjects from './CardProjects.vue';

export default {
  name: 'PortfolioPedro',
  data() {
    return {
      age: 23,
      ibnaName: 'SITE IBNA',
      ibnaText: 'Site criado para a IBNA SCS, feito em PHP e JS e Bootstrap utilizando o tema Assan.',
      ibnaImg: require('../assets/png/logo-ibna.png'),
      ibnaLink: 'https://ibnagapescs.com.br',
      solutioName: 'SOLUTIO',
      solutioText: 'Participei da criação de diversos softwares de segurança privada utilizando tecnologias como: PHP, JS, HTML, CSS, MySql, Docker, etc...',
      solutioImg: require('../assets/png/logo-solutio.png'),
      solutioLink: 'https://solutiosoftware.com.br',
      dayzName: 'DAYZ STATS',
      dayzText: 'API feita em PHP para exportar status de jogadores de um servidor de DayZ para um dashboard personalizado na web.',
      dayzImg: require('../assets/jpeg/logo-dayz.jpeg'),
      dayzLink: 'https://github.com/pedrohstaub/dayz_stats',
      portfolioName: 'Portfolio',
      portfolioText: 'Portfólio feito em VueJS para demonstrar minha familiaridade com a tecnologia e expor meus projetos pessoais e profissionais.',
      portfolioImg: require('../assets/png/vue-logo.png'),
      portfolioLink: 'https://github.com/pedrohstaub/portfolio'
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
  border-color: #303030;
  height: 1px;
}

.tech>img {
  width: 10%;
  min-width: 80px;
  margin: 2%;
}

.tech>img:hover {
  animation: tech-animate 200ms;
  animation-fill-mode: forwards;
}

.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around !important;
  width: 100%;
}

.content {
  margin: 10%;
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

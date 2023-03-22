<template>
  <div class="content">
    <div id="about">
      <hr>
      <h1 v-html="$t('portfolio.title')"></h1>
      <h3 v-html="$t('portfolio.text1', { age: this.age })"></h3>
      <h3 style="text-align:center" v-html="$t('portfolio.text2')"></h3>

      <br />
      <hr>
    </div>
    <div id="tech">
      <h1 v-html="$t('portfolio.title2')"></h1>
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
      <h1 v-html="$t('portfolio.title3')"></h1>
      <br />
      <div class="projects">
        <card-projects :titleCard="$t('projects.ibna.name')" :text="$t('projects.ibna.text')"
          :img="require('../assets/png/logo-ibna.png')" link="https://ibnagapescs.com.br">
        </card-projects>
        <card-projects :titleCard="$t('projects.solutio.name')" :text="$t('projects.solutio.text')"
          :img="require('../assets/png/logo-solutio.png')" link="https://solutiosoftware.com.br">
        </card-projects>
        <card-projects :titleCard="$t('projects.dayz.name')" :text="$t('projects.dayz.text')"
          :img="require('../assets/jpeg/logo-dayz.jpeg')" link="https://github.com/pedrohstaub/dayz_stats">
        </card-projects>
        <card-projects :titleCard="$t('projects.portfolio.name')" :text="$t('projects.portfolio.text')"
          :img="require('../assets/png/vue-logo.png')" link="https://github.com/pedrohstaub/portfolio">
        </card-projects>
        <card-projects :titleCard="$t('projects.discord.name')" :text="$t('projects.discord.text')"
          :img="require('../assets/png/discord-logo.png')" link="https://github.com/pedrohstaub/discord_login">
        </card-projects>
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
      age: 1
    }
  },
  methods: {
    defineAge() {
      let year = new Date().getFullYear();
      this.age = year - 1999;
    }
  },
  created() {
    this.defineAge();
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

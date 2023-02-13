<template>
    <header id="header">
        <div class="content">
            <NavBar />
            <div class="div-content">
                <img src="@/assets/jpeg/18274435.jpeg" alt="Pedro">
                <!-- <img src="@/assets/png/teste.png" alt="Pedro"> -->
                <h1>Pedro Henrique Staub</h1>
                <h3>Desenvolvedor Web FullStack</h3>
                <a class="social" href="https://github.com/pedrohstaub" target="_blank">
                    <i class="devicon-github-original"></i>
                    GitHub
                </a>&nbsp;
                <a class="social" href="https://www.linkedin.com/in/pedro-henrique-staub-962141101/" target="_blank">
                    <i class="devicon-linkedin-plain"></i>
                    LinkedIn
                </a>
            </div>
        </div>
    </header>
</template>

<script>
import NavBar from './NavBar.vue';

export default {
    name: "HeaderComponent",
    components: {
        NavBar
    }
}
</script>

<style scoped>
img {
    float: right;
}

.content {
    /* background-image: url("@/assets/png/bg1.png");
    background-repeat: no-repeat;
    background-size: cover; */
    height: 60vh;
    margin: 0 !important;
    background: linear-gradient(-50deg, #2d2dfa, #00A0DF, #00005c,#000);
    background-size: 400% 400%;
    animation: gradient 25s ease infinite;
}

@keyframes gradient {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

.div-content {
    padding-bottom: 10%;
    padding-top: 10%;
    text-align: left;
    margin: 5%;
    margin-top: 0 !important;
}

.div-content>img {
    /* text-align: left; */
    border-radius: 50%;
    width: 33vh
}

a {
    text-decoration: none !important;
}

.social {
    border: solid 2px white;
    padding: 0.5%;
    text-decoration: none !important;
    border-radius: 20px;
    color: white;
    font-size: 125%;
    font-weight: bold;
}

.social:hover {
    animation: animation-button 500ms;
    animation-fill-mode: forwards;
}

@keyframes animation-button {
    0% {
        font-size: 130%;
    }

    50% {
        font-size: 135%;
    }

    75% {
        font-size: 140%;
    }

    100% {
        font-size: 145%;
        padding: 10px;
    }
}

.div-content>img:hover {
    border: 2px solid white;
    animation: hover-img 100ms;
    animation-fill-mode: forwards;
}

@keyframes hover-img {
    0% {
        width: 37vh;
        padding: 3px;
    }

    25% {
        width: 40vh;
        padding: 5px;
    }

    50% {
        width: 43vh;
        padding: 7px;
    }

    75% {
        width: 45vh;
        padding: 10px;
    }

    100% {
        width: 47vh;
        padding: 12px;
    }
}
</style>
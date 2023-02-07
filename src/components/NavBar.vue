<template>
    <div class="teste">
        <nav class="flex-container">
            <span class="material-icons md-48">developer_mode</span>
            <div>
                <ul>
                    <li class="flex-container-item-main"><a href="#header">Contato</a></li>
                    <li class="flex-container-item-main"><a href="#about">Sobre</a></li>
                    <li class="flex-container-item-main"><a href="#tech">Tecnologias</a></li>
                    <li class="flex-container-item-main"><a href="#projects">Projetos</a></li>
                    <li class="flex-container-item-main"><a href="#projects">Projetos</a></li>
                </ul>
            </div>
        </nav>
        <!-- <hr style="border: 0; border-top: 1px solid #CCC; margin: 1%"> -->
    </div>
</template>

<script>

export default {
    name: "NavBar",
}
</script>

<style scoped>
nav {
    backdrop-filter: blur(3px);
    width: 100% !important;
    position: fixed;
    margin: 0 !important;
    border-bottom: 2px solid #54545465;
}

li {
    display: inline-block;
    margin: 1%;
}

a {
    text-decoration: none;
    width: 100%;
}

.flex-container {
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-around !important;
    width: 100%;
}

.flex-container-item-main {
    background-image: linear-gradient(to right, hwb(221 0% 13%), rgb(0, 160, 223));
    width: 120px;
    margin: 10px;
    text-align: center;
    line-height: 230%;
    border-radius: 20px;
    /* border: 1px solid white; */
}

.flex-container-item-main>a {
    color: white;
}

.flex-container-item {
    background-color: rgb(222, 222, 222);
    width: 120px;
    margin: 10px;
    text-align: center;
    line-height: 230%;
    border-radius: 20px;
}

.flex-container-item>a {
    color: hwb(221 0% 13%);
}

.flex-container-item:hover {
    background-color: hwb(221 0% 7% / 0.767);
    cursor: pointer;

}

.flex-container-item-main:hover {
    background-color: hwb(221 0% 7% / 0.767);
    cursor: pointer;
    border: 1.5px solid #fff;
    animation: animation-button 100ms;
    animation-fill-mode: forwards;
}

.material-icons.md-48 {
    background-image: linear-gradient(to right, hwb(221 0% 13%), rgb(0, 160, 223));
    color: white;
    font-size: 35px;
    width: 90px;
    margin: 10px;
    text-align: center;
    line-height: 230%;
    border-radius: 20px;
}

.material-icons.md-48:hover {
    background-color: hwb(221 0% 7% / 0.767);
    cursor: pointer;
}

@keyframes animation-button {
    0% {
        font-size: 100%;
    }

    50% {
        font-size: 105%;
    }

    75% {
        font-size: 108%;
    }

    100% {
        font-size: 112%;
    }
}
</style>
<template>
    <nav>
        <span class="material-icons md-48">terminal</span>
        <div class="mobile-menu" @click="teste">
            <div class="line1"></div>
            <div class="line2"></div>
            <div class="line3"></div>
        </div>
        <div>
            <ul class="nav-list">
                <li class="menu-item"><a href="#header">{{ $t('nav.b1') }}</a></li>
                <li class="menu-item"><a href="#about">{{ $t('nav.b2') }}</a></li>
                <li class="menu-item"><a href="#tech">{{ $t('nav.b3') }}</a></li>
                <li class="menu-item"><a href="#projects">{{ $t('nav.b4') }}</a></li>
                <li class="menu-item"><a :href="$t('nav.cvLink')" target="_blank">{{ $t('nav.b5') }}</a></li>
                <li class="menu-flag"><a href="#" @click="setLocale('pt_br')"><img class="flag" src="https://flagsapi.com/BR/flat/32.png"></a></li>
                <li class="menu-flag"><a href="#" @click="setLocale('en')"><img class="flag" src="https://flagsapi.com/US/flat/32.png"></a></li>
            </ul>
        </div>
    </nav>
</template>

<script>

export default {
    data() {
        return {
            mobileMenu: '.mobile-menu'
        }
    },
    name: "NavBar",
    methods: {
        teste: function () {
            let navList = document.querySelector(".nav-list");
            console.log(this.mobileMenu);
            navList.classList.toggle('active');
        },
        setLocale(locale){
            this.$i18n.locale = locale;
        }
    }
}
</script>

<style scoped>
nav {
    backdrop-filter: blur(3px);
    width: 100% !important;
    position: fixed;
    margin: 0 !important;
    border-bottom: 2px solid #54545465;
    height: 12vh;
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-around !important;
}

li {
    display: inline-block;
    margin: 1%;
}

a {
    text-decoration: none;
    width: 100%;
    letter-spacing: 1px;
}

.menu-item {
    background-image: linear-gradient(to right, #2d2dfa, #00A0DF);
    width: 120px;
    margin: 10px;
    text-align: center;
    line-height: 230%;
    border-radius: 20px;
    /* border: 1px solid white; */
}

.menu-flag {
    width: 50px;
    margin: 10px;
    text-align: center;
    line-height: 230%;
    border-radius: 20px;
    vertical-align: middle;
}

.menu-item>a {
    color: white;
}

.menu-item-alternative {
    background-color: rgb(222, 222, 222);
    width: 120px;
    margin: 10px;
    text-align: center;
    line-height: 230%;
    border-radius: 20px;
}

.menu-item-alternative>a {
    color: hwb(221 0% 13%);
}

.menu-item-alternative:hover {
    background-color: hwb(221 0% 7% / 0.767);
    cursor: pointer;

}

.menu-item:hover {
    background-color: #0068d6;
    cursor: pointer;
    border: 1.5px solid #fff;
    animation: animation-button 100ms;
    animation-fill-mode: forwards;
}

.material-icons.md-48 {
    background-image: linear-gradient(to right, #2d2dfa, #00A0DF);
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

.mobile-menu {
    cursor: pointer;
    display: none;
}

.mobile-menu div {
    width: 32px;
    height: 2px;
    background: #fff;
    margin: 10px;
}

@media (max-width: 1000px) {
    body {
        overflow-x: hidden;
    }

    nav {
        height: 8vh;
        justify-content: flex-end
    }

    .nav-list {
        position: absolute;
        top: 10vh;
        right: 20px;
        width: 35vw;
        height: 92vh;
        backdrop-filter: blur(3px);
        transform: translateX(100%);
        transition: transform 0.2s ease-in;
    }

    .nav {
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
    }

    .mobile-menu {
        display: block;
        margin-right: -55%;
        margin-top: 3%;
    }

    .nav-list.active {
        transform: translateX(0);
    }

    .menu-flag {
        width: 160px;
    }
    .menu-item {
        width: 160px
    }

    .flag{
        width: 50px;
    }
    .material-icons.md-48 {
        background-image: linear-gradient(to right, #2d2dfa, #00A0DF);
        color: white;
        font-size: 20px;
        width: 55px;
        /* margin: 10px; */
        text-align: center;
        line-height: 230%;
        border-radius: 10px;
        margin-left: -50px !important;
    }
}
</style>
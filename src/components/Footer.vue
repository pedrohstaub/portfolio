<template>
    <footer>
        <hr>
        <div class="flex">
            <a href="mailto:ppedrohstaub@gmail.com">
                <span class="material-icons">
                    email
                </span>
                {{ $t('footer.b1') }}
            </a>
            <a href="https://api.whatsapp.com/send?phone=5551997177824&text=Olá">
                <span class="material-icons">
                    phone_android
                </span>
                {{ $t('footer.b2') }}
            </a>
            <a class="social" href="https://www.linkedin.com/in/pedro-henrique-staub-962141101/" target="_blank">
                <i class="devicon-linkedin-plain"></i>
                {{ $t('footer.b3') }}
            </a>
            <a class="social" href="https://github.com/pedrohstaub" target="_blank">
                <i class="devicon-github-original"></i>
                {{ $t('footer.b4') }}
            </a>
        </div>
    </footer>
</template>

<script>
export default {
    name: "FooterComponent"
}
</script>

<style scoped>
footer {
    margin: 3%
}

hr {
    border-color: #303030;
    margin-bottom: 2%
}

a {
    text-decoration: none;
    color: #ccc;
    font-size: 20px !important
}

.flex {
    display: flex;
    justify-content: space-around;
}

.material-icons {
    color: white;
    vertical-align: middle;
}
</style>
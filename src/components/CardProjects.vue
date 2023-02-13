<template>
    <div class="card-outter">
        <div class="card-inner">
            <div class="card-header">
                <a :href="link" target="_blank" :title="titleCard" :alt="titleCard"><img :src="img" /></a>
                <!-- <p><b>{{ titleCard }}</b></p> -->
            </div>
            <div class="card-body">
                <p>{{ text }}</p>
            </div>
            <hr>
            <div class="card-footer">
                <a v-if="link" :href="link" target="_blank"><span class="material-icons">public</span> Acesse </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        titleCard: {
            type: String,
            required: true,
            default: 'Title stays here'
        },
        text: {
            type: String,
            required: true,
            default: 'This is the text for the body'
        },
        link: {
            type: String,
            required: false,
            default: '',
        },
        img: {
            type: String,
            required: true,
            default: require('@/assets/png/Stargate.png')
        },
        data(){
            return{
                showLink: false
            }
        },
        methods:{
            verifyLink(){
                if(this.link != '#'){
                    this.showLink = true;
                }
            }
        }
    }
}
</script>

<style scoped>
.card-outter {
    width: 47%;
    height: 286px;
    max-width: 500px;
    min-width: 350px;
    max-height: 400px;
    min-height: 100px;
    padding: 1rem;
    background: linear-gradient(to right, #2d2dfa, #00A0DF);
    padding: 3px;
    margin-bottom: 2%;
    border-radius: 5px;
}

.card-inner {
    color: white;
    padding: 2rem;
    background: rgb(23, 23, 23);
    min-height: 220px;
    max-height: 200px !important;
    overflow: hidden;
}

.image {
    width: 20%;
    /* height: ; */
}

.card-header {
    font-size: 200%;
    vertical-align: middle;
    justify-content: space-evenly !important;
    display: flex;
}

.card-footer {
    vertical-align: middle;
}

.card-footer>a>span {
    vertical-align: middle;
}
.card-footer>a {
    text-decoration: none;
    color: #fff;
}

.card-header>a>img {
    width: 30%;
    overflow: hidden;
    /* height: 10%; */
}

.card-inner>p {
    text-align: left
}

.module {
    background: #000000;
    color: white;
    padding: 2rem;
}
</style>
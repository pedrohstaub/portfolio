<template>
    <p>{{ titleCard }}</p>
    <p>{{ text }}</p>
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
        link:{
            type: String,
            required: false,
            default: 'Link to the project'
        }
    }
}
</script>

<style scoped>

</style>
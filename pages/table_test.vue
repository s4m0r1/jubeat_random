<template>
    <p>{{ results }}</p>
</template>

<script>
export default {
    data() {
        return {
            results: process.env.SONGJSONURL
        }
    },
    async asyncData({ app }) {
        const songJsonUrl = process.env.SONGJSONURL
        console.log(songJsonUrl)
        const response = await app.$axios.$get(songJsonUrl)
    },
}
</script>

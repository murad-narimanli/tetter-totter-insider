<template>
    <main class="gameArea">
        <DropboxElement/>
        <TeetleTottle/>
    </main>
</template>

<script>
    import TeetleTottle from './TeetleTottle'
    import DropboxElement from "@/components/Dropbox.vue";

    export default {
        name: "GameArea",
        components:{
          DropboxElement,
          TeetleTottle
        }
    }
</script>

<style lang="scss" scoped>
    .gameArea {
        width: 80%;
        height: 100%;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        padding-top: 1rem;
    }
</style>

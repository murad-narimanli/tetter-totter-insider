<template>
    <section class="teetleTottle">
        <SwingElement/>
        <PillarElement/>
    </section>
</template>

<script>
    import SwingElement from "@/components/Swing.vue";
    import PillarElement from "@/components/Pillar.vue";

    export default {
        name: "TeetleTottle",
        components: {
          PillarElement,
          SwingElement,
        }
    }
</script>

<style scoped>
    .teetleTottle{
        height: 35%;
        width: 100%;
    }
</style>

<template>
    <div class="swing" :style="inlineStyleSwing">
        <BlockElement v-for="block in leftSideBlocks"
               :block="block"
               :key="block.id"/>
        <BlockElement v-for="block in rightSideBlocks"
               :block="block"
               :side="true"
               :key="block.id"/>
    </div>
</template>

<script>
    import {mapState, mapMutations} from 'vuex'
    import {ADD_RIGHT_SIDE_BLOCK} from '../constants'
    import BlockElement from "@/components/Block.vue";

    export default {
        name: "SwingElement",
        components: {
          BlockElement,
        },
        computed: {
            ...mapState([
                'rightSideBlocks',
                'leftSideBlocks'
            ]),
            swingBending() {
                return this.$store.getters.swingBending
            },
            inlineStyleSwing() {
                return {
                    transform: `rotate(${this.swingBending / 2}deg)`
                }
            }
        },
        methods: {
            ...mapMutations({
                addRightBlock: ADD_RIGHT_SIDE_BLOCK,
            })
        },
        beforeMount() {
            this.addRightBlock()
        }
    }
</script>

<style lang="scss" scoped>
    .swing {
        width: 100%;
        height: 0.5rem;
        background-color: #263238;
        position: relative;
        transform: rotate(0deg);
        transition: transform 0.4s ease-in-out;
    }
</style>

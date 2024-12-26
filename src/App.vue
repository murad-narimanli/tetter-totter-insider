<template>
  <div class="root">
    <HeaderTop/>
    <GameArea/>
  </div>
</template>

<script>
import GameArea from '@/components/GameArea'
import HeaderTop from "@/components/Header";

export default {
  name: 'App',
  components: {
    HeaderTop,
    GameArea
  }
}
</script>

<style lang="scss">
.root {
  overflow: hidden;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}
</style>

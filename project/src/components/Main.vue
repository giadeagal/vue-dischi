<template>
  <main>
      <div class="container">
          <Card prova="Hey!"/>
      </div>
  </main>
</template>

<script>
import Card from '.././components/Card.vue';

export default {
  name: 'Main',
  components: {
      Card
  }
}
</script>

<style lang="scss" scoped>
@import "../styles/vars.scss";

main {
    background-color: $spotiblue;
    height: calc(100vh - 50px);
    display: flex;
    align-items: center;

    .container {
        background-color: red; //debug
        height: 400px;  //debug
    }
}


</style>
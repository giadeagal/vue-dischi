<template>
  <main>
      <div class="container">
          <div class="row justify-content-between">
              <div class="col-3">
                  <Card prova="Hey!"/>
              </div>
              <div class="col-3">
                  <Card prova="Hey!"/>
              </div>
              <div class="col-3">
                  <Card prova="Hey!"/>
              </div>
          </div>
      </div>
  </main>
</template>

<script>
import Card from '.././components/Card.vue';
import axios from "axios";

export default {
  name: 'Main',
  components: {
      Card
  },
  data() {
      return {
          apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
          albumList: []
      }
    },
    created() {
        this.getAlbum();
    },
    methods: {
        getAlbum() {
            axios
                .get(this.apiURL)
                .then (x => {
                    console.log(x)
                })
        }
    }
};
</script>

<style lang="scss" scoped>
@import "../styles/vars.scss";

main {
    background-color: $spotiblue;
    height: calc(100vh - 50px);
    display: flex;
    align-items: center;

    .container {
        height: 400px;  //debug
    }
}

.col-3 {
    border: 1px dashed teal;  //debug
    max-height: 80px;
    padding-top: 20px;
    color: white;  //debug
}


</style>
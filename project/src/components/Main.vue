<template>
  <main>
      <div class="container">
          <div class="row justify-content-around">
              <div v-for="(e, i) in albumList" :key="i" class="col-2 m-2">
                  <Card :album="e"/>
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
                    this.albumList = x.data.response;
                    console.log(this.albumList);
                })
        }
    }
};
</script>

<style lang="scss" >
@import "../styles/vars.scss";

main {
    background-color: $spotiblue;
    height: 100%;
    display: flex;
    align-items: center;

    .container {
        height: 100%;
        margin-top: 50px;
    }
}

.col-2 {
    padding: 20px 0;
    background-color: $spotigray;
    h3 {
        font-size: 1.3rem;
        color: #fff;
        font-weight: 700;
    }

    small {
        color: gray;
    }
}


</style>
<template>
    <div class="alb">
        <img :src="album.poster" alt="album.title">
      <h3 class="py-3">{{album.title}}</h3>
      <p>
        {{album.author}} <br>
        {{album.year}}
      </p>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["album"]
}
</script>

<style lang="scss">


img {
    max-width:100%
}

h3,p {
    text-align: center;
}

h3 {
    text-transform: uppercase;
}

p {
    color: gray;
}

</style>
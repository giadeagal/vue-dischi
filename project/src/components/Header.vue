<template>
  <header>
    <img src="@/assets/logo.png" alt="spotify web">
  </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style lang="scss" scoped>
    @import "../styles/vars.scss";

    header {
        height: 50px;
        background-color: $spotigray;
    }

    img {
        width: 45px;
        padding:5px;
    }


</style>
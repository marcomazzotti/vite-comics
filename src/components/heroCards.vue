<script>
export default{
  name: "heroCards",
  props:{
    image: String,
    title: String
  }
}
</script>

<template>
  <div class="card">
    <img :src="image" alt="">
    <h5>{{ title }}</h5>
  </div>
</template>

<style scoped lang="scss">
  .card{
    width: calc(100% / 6 - 10px);
    margin: 5px;
    // margin-bottom: -30px;
    // background-color: wheat;

    img{
      height: 70%;
      object-fit: cover;
      object-position: 100% 0%;
    }
  }
</style>
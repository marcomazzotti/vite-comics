<script>
export default {
  name: "appHeader"
}
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <div class="menu">
        <ul class="menu-items">
          <li>CHARACTERS</li>
          <li>COMICS</li>
          <li>MOVIES</li>
          <li>TV</li>
          <li>GAMES</li>
          <li>COLLECTIBLES</li>
          <li>VIDEOS</li>
          <li>FANS</li>
          <li>NEWS</li>
          <li>SHOP</li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
  header{
    height: 90px;
    display: flex;
    align-items: center;
    // border: 1px solid red;
  }

  .container{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .logo{
    width: 60px;
  }

  .menu-items{
    display: flex;
    list-style-type: none;
    font-size: 0.8rem;

    li {
      padding-left: 1rem;
    }
  }
</style>
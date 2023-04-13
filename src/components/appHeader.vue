<script>
export default {
  name: "appHeader",
  data(){
    return {
      links: [
        {
          text: "CHARACTERS",
          url: "#",
          current: false
        },
        {
          text: "COMICS",
          url: "#",
          current: true
        },
        {
          text: "MOVIES",
          url: "#",
          current: false
        },
        {
          text: "TV",
          url: "#",
          current: false
        },
        {
          text: "GAMES",
          url: "#",
          current: false
        },
        {
          text: "COLLECTIBLES",
          url: "#",
          current: false
        },
        {
          text: "VIDEOS",
          url: "#",
          current: false
        },
        {
          text: "FAN",
          url: "#",
          current: false
        },
        {
          text: "NEWS",
          url: "#",
          current: false
        },
        {
          text: "SHOP",
          url: "#",
          current: false
        },
      ]
    }
  }
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
          <li v-for="link in links" :class="link.current ? 'active' : ''">
            <a href="{{ link.url }}">{{ link.text }}</a>
            <div v-show="link.current" class="active-bar"></div>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

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
    width: 20%;

    img{
      width: 60px;
    }
  }

  .menu-items{
    display: flex;
    list-style-type: none;
    font-size: 0.8rem;
    gap: 1.3rem;

    li{
      color: black;
      position: relative;
      line-height: 85px;
      
      &.active, &:hover{
        color: $primary;
        border-bottom: 5px solid $primary;
      }

      a {
      text-decoration: none;
      color: inherit;
      }

      .active-bar{
        width: 100%;
        height: 5px;
        background-color: $primary;
        position: absolute;
        bottom: 90px;
      }
    }
  }
</style>
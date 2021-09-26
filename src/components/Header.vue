<template>
  <header>
    <a href="#" class="dc_logo">
      <img src="@/assets/img/dc-logo.png" alt="">
    </a>
    <nav>
      <ul>
        <li v-for="(link, index) in links" :key="index">
          <a :class="(link.current) ? 'active': null" :href="link.url">{{link.text.toUpperCase()}}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  
  data() {
    return {
      links: [
        {
          text: "Characters",
          url: "#",
          current: false
        },
        {
          text: "Comics",
          url: "#",
          current: true
        },
        {
          text: "Movies",
          url: "#",
          current: false
        },
        {
          text: "Tv",
          url: "#",
          current: false
        },
        {
          text: "Games",
          url: "#",
          current: false
        },
        {
          text: "Collectibles",
          url: "#",
          current: false
        },
        {
          text: "Videos",
          url: "#",
          current: false
        },
        {
          text: "Fans",
          url: "#",
          current: false
        },
        {
          text: "News",
          url: "#",
          current: false
        },
        {
          text: "Shop",
          url: "#",
          current: false
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "@/style/generals.scss";

header {
  padding: 22px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;

  ul {
    list-style: none;
    display: flex;
    font-weight: 600;

    li a {
      padding: 3.8rem 1rem;
      text-decoration: none;
      color: black;

      &:hover, &:active {
        color: #0282F9;
        border-bottom: 5px solid #0282F9;
      }
    }
  }
}



</style>

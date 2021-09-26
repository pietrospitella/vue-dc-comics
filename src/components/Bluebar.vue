<template>
  <div class="bluebar">
      <ul id="bluebar_cont">
        <li v-for="(opt, index) in options" :key="index">
          <img id="opt" :src="require(`../${opt.img}`)" alt="">
          <a :href="opt.url">{{opt.name.toUpperCase()}}</a>
        </li>
      </ul>
  </div>
</template>

<script>

export default {
  name: 'BlueBar',
  data() {
    return {
      options: [
        {
          name: "Digital Comics",
          url: "#",
          img: "assets/img/buy-comics-digital-comics.png"
        },
        {
          name: "DC Merchandise",
          url: "#",
          img: "assets/img/buy-comics-merchandise.png"
        },
        {
          name: "Subscription",
          url: "#",
          img: "assets/img/buy-comics-subscriptions.png"
        },
        {
          name: "Comic Shop Locator",
          url: "#",
          img: "assets/img/buy-comics-shop-locator.png"
        },
        {
          name: "DC Power Visa",
          url: "#",
          img: "assets/img/buy-dc-power-visa.svg"
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.bluebar{
  background-color: #0282F9;
  
  #bluebar_cont{
    list-style: none;
    color: white;
    height: 10rem;
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;

    li {
      margin: 0 20px;
      display: flex;
      align-items: center;
    }

    img {
      height: 50px;
    }

    &::before{
      content: "";
    }

    a {
      text-decoration: none;
      color: white;
      margin-left: 10px;
    }

  }
}


</style>

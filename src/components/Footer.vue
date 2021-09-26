<template>
  <div class="footer">
    <div id="footer_top">
      <div id="top_cont">
        <div id="lists_cont">
          <div v-for="(link, index) in links" :key="index" class="list">
            <h4>{{link.group}}</h4>
            <ul>
              <li v-for="(item, index) in link.items" :key="index">
                <a href="links.items[index].url">{{link.items[index].name}}</a>
              </li>
            </ul>
          </div>        
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div id="footer_bottom">
      <div id="bottom_cont">
        <button id="sign_up_button"><a href="#">Sign-up now!</a></button>
        <div id="socials">
          <h6>follow us</h6>
          <ul>
            <li v-for="(social, index) in socials" :key="index">
              <a href="#"><img :src="require(`../assets/img/footer-${social.name}.png`)" alt=""></a>                            
            </li>
          </ul>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      links: [
        {
          group: "dc comics",
          items: [
            {
              name: "Characters",
              url: "#"
            },
            {
              name: "Comics",
              url: "#"
            },
            {
              name: "Movies",
              url: "#"
            },
            {
              name: "Tv",
              url: "#"
            },
            {
              name: "Games",
              url: "#"
            },
            {
              name: "Videos",
              url: "#"
            },
            {
              name: "News",
              url: "#"
            }
          ],
        },
        {
          group: "shop",
          items: [
            {
              name: "Shop DC",
              url: "#"  
            },
            {
              name: "Shop DC Collectibles",
              url: "#"  
            }
          ],
        },
        {
          group: "dc",
          items: [
            {
              name:"Terms Of Use",
              url: "#"  
            },
              
            {
              name:"Privacy policy (New)",
              url: "#"  
            },
              
            {
              name:"Ad Choices",
              url: "#"  
            },
              
            {
              name:"Advertising",
              url: "#"  
            },
              
            {
              name:"Jobs",
              url: "#"  
            },
              
            {
              name:"Subscriptions",
              url: "#"  
            },
              
            {
              name:"Talent Workshops",
              url: "#"  
            },
              
            {
              name:"CPSC Certificates",
              url: "#"  
            },
              
            {
              name:"Ratings",
              url: "#"  
            },
              
            {
              name:"Shop Help",
              url: "#"  
            },
              
            {
              name:"Contact Us",
              url: "#"
            }
              
          ],
        },
        {
          group: "sites",
          items: [
            {
              name: "DC",
              url: "#"
            },
            {
              name: "MAD Magazine",
              url: "#"
            },
            {
              name: "DC Kids",
              url: "#"
            },
            {
              name: "DC Universe",
              url: "#"
            },
            { name: "DC Power Visa",
              url: "#"
            }
          ],
        },
      ],
      socials: [
        {
          name: "facebook",
        },
        {
          name: "twitter",
        },
        {
          name: "youtube",
        },
        {
          name: "pinterest",
        },
        {
          name: "periscope",
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

#footer_top {
  height: 20rem;
  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;
  overflow: hidden;
  color: white;
  display: flex;
  align-items: center;
  position: relative;

  #top_cont{
    width: 80%;
    margin: 0 auto;
    height: 100%;
    display: flex;
    align-items: center;

    #lists_cont {
      height: 80%;
      width: 40%;
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;

      h4 {
        text-transform: uppercase;
        margin-bottom: 10px;
      }

      ul {
        list-style: none;
        margin-bottom: 10px;
      }

      li a {
        color: gray;
        text-decoration: none;
        font-size: 13px;
      }

      img {
        position: absolute;
        top: -80px;
        right: 10%;
        height: 28rem;      
      }
    }

  }

}

#footer_bottom {
  height: 5.5rem;
  background-color: #333333;
  display: flex;
  align-items: center;


  #bottom_cont{
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;

    button {
      height: 50px;
      width: 120px;
      border: 3px solid #0282F9;
      background-color: #333333;
      text-transform: uppercase;

      a {
        color: white;
        text-decoration: none;
      }
    }

    #socials{
      display: flex;
      align-items: center;
    
      h6 {
      color: #0282F9;
      text-transform: uppercase;
      font-size: 16px;
      margin-right: 15px;
      }

      ul {
      display: flex;
      list-style: none;
      }

      li {
        padding: 10px;
      }
    }
  }
}

</style>

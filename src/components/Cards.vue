<template>
  <div>
    <div id="cards">
      <div id="cards_cont">
        <div v-for="(comic, index) in comics" :key="index" id="single_card">
          <div id="img_box">
            <img :src="comic.thumb" alt="">
          </div>
          <h4>{{comic.series}}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import comicsList from '../data/dc-comics.json';

export default {
  name: 'Cards',
  data() {
    return {
      comics: comicsList
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

#cards {
  height: 50rem;
  background-color: #1C1C1C;
  display: flex;
  align-items: center;
  position: relative;

  &::before{
    width: 150px;
    height: 20px;
    background-color: #0282F9;
    color: white;
    font-size: 18px;
    font-weight: 900;
    padding: 15px 35px;
    content: "CURRENT SERIES";
    position: absolute;
    top: -20px;
    left: 10%;
  }

  &::after{
    width: 150px;
    height: 20px;
    background-color: #0282F9;
    color: white;
    font-size: 18px;
    font-weight: 900;
    padding: 15px 35px;
    content: "LOAD MORE";
    text-align: center;
    position: absolute;
    bottom: 40px;
    left: 44vw;
    cursor: pointer;
  }

  #cards_cont {
    height: 80%;
    width: 80%;
    margin: 0 auto;
    position: relative;
    // border: 1px solid white;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    flex-wrap: wrap;
    
    #single_card {
      // border: 1px solid greenyellow;
      display: flex;
      flex-direction: column;
      justify-content: center;
      width: calc((80vw / 6) - 5px);

      #img_box{
        width: calc(14vw - 30px);
        max-width: 250px;
        height:  calc(14vw - 30px) ;
        max-height: 250px;
        overflow: hidden;
        // border: 1px solid red;

        img {
          width: 100%;
        }

      }
      
      h4 {
        align-self: flex-start;
        color: white;
        text-transform: uppercase;
        margin: 10px 0;
      }

    }

  }

}



</style>

<template>
  <div id="app">
    <Header/>
    <main>
      <Content />
      <Cards />
      <Bluebar />
    </main>
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Content from '@/components/Content.vue'
import Cards from '@/components/Cards.vue'
import Bluebar from '@/components/Bluebar.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Content,
    Cards,
    Bluebar,
    Footer
  }
}
</script>

<style lang="scss">

@import "@/style/generals.scss";


</style>

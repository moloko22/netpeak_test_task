<template>
  <div id="app">
    <section class="application">
      <Header></Header>
      <Main></Main>
      <WhyUse></WhyUse>
      <Footer></Footer>
    </section>
  </div>
</template>
<script>
  import Header from './components/Header/Header.vue';
  import Footer from './components/Footer/Footer';
  import Main from "@/components/Main/Main";
  import WhyUse from "@/components/WhyUse/WhyUse";
export default {
  name: 'App',
  components: {
    WhyUse,
    Header,
    Main,
    Footer
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
  .application{
    position: relative;
    margin-top: -10px;
    width: 1440px;
    min-height: 2470px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  #app {
    width: 100%;
    min-height: 2470px;
    display: flex;
    justify-content: center;
  }
</style>

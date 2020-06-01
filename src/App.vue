<template>
  <div id="app">
    <Header></Header>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>
<script>
  import Header from './components/Header/Header.vue';
  import Footer from './components/Footer/Footer';
  import Main from "@/components/Main/Main";
export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style>
  #app {
    width: 1440px;
    min-height: 2570px;
  }
  *{
    margin: 0;
    padding: 0;
  }
</style>

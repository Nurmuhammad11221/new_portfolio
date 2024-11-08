<template>
    <Nav />
    <Header />
    <About/>
    <!-- <Main />
    <Footer /> -->
  </template>
  
  <script>
  import Nav from './components/Nav.vue';
  import Header from './components/Header.vue';
  import About from './components/About.vue';
//   import Main from './components/Main.vue';
//   import Footer from './components/Footer.vue';
  
  
  export default {
    components: {
      Nav,
      Header,
      About
    //   Main,
    //   Footer
    },
  };
  </script>
  
<style>
    *{
      padding: 0;
      margin: 0;
      text-decoration: none;
    }
  
</style>
  
<template>
    <Nav />
    <Header />
    <About/>
    <Konikmalar />
    <Main />
    <Footer /> 
  </template>
  
  <script>
  import Nav from './components/Nav.vue';
  import Header from './components/Header.vue';
  import About from './components/About.vue';
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';
import Konikmalar from './components/Konikmalar.vue';
  
  
  export default {
    components: {
      Nav,
      Header,
      About,
      Konikmalar,
      Main,
      Footer
    },
  };
  </script>
  
<style>
    *{
      padding: 0;
      margin: 0;
      text-decoration: none;
    }

    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      display: flex;
      flex-direction: column;
  }

  /* Asosiy App konteyneri */
  .app {
      display: flex;
      flex-direction: column;
      min-height: 100vh;
  }

  /* MainComponent ning yuqorida bo'lishini va Footer ning pastda joylashishini ta'minlash */
  .app > *:first-child {
      flex: 1;
  } 
  
</style>
  
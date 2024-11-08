<template>
    <div  class="nav__container">
        <div class="right__nav">

            <h1>FINEDEV.uz</h1>

        </div>

        <div class="left__nav">
            <li>
                <a class="nav__link" href="#home">Bosh Sahifa</a>
            </li>

            <li>
                <a class="nav__link" href="">Men haqimda</a>
            </li>

            <li>
                <a class="nav__link" href="">Ko'nikmalar</a>
            </li>

            <li>
                <a class="nav__link" href="">Xizmatlar</a>
            </li>

            <li>
                <a class="nav__link" href="">Portfolio</a>
            </li>

            <li>
                <a class="nav__link" href="">Bog'lanish</a>
            </li>


        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      showContent: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showContent = true;
    }, 500);
  },
  data() {
    return {
      isNavbarOpen: false
    };
  },
  methods: {
    toggleNavbar() {
      this.isNavbarOpen = !this.isNavbarOpen;
    }
  }
  
};
</script>

<style scoped>

    .fade-enter-active, .fade-leave-active {
        transition: opacity 1s;
    }
    .fade-enter, .fade-leave-to  {
        opacity: 0;
    }
    .nav__container{
        height: 65px;
        color: white;
        background-color: blue;
        display: flex;
        justify-content: space-around;
        animation: fadeIn 1s ease-in-out 0.5s; 
    }

    .right__nav{
        display: flex;
        color: white;
        align-items: center;
    }

    .left__nav{
        display: flex;
        align-items: center;
        list-style-type: none;
        gap: 40px;
    }

    .nav__link{
        color: white ! important;
        align-items: center;
        transition: 0.3s;
    }

    .nav__link:hover{
        color: black ! important;

    }

    .toggle-button {
        font-size: 1.5rem;
        background: none;
        border: none;
        color: white;
        cursor: pointer;
      }

   

    @media (max-width: 768px) {


        .nav__container{
            height: 100px;
            display: block;
        }

        .navbar-links {
            display: flex;
            flex-direction: row;
          }
          .toggle-button {
            display: none;
          }

            
        
    }
</style>
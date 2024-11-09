<template>
    <div class="nav__container" :class="{ 'scrolled': isScrolled }">
      <button class="toggle-button" @click="toggleNavbar">
        ☰
      </button>
  
      <div class="left__nav">
        <h1>FINEDEV.uz</h1>
  
        <ul :class="['menu', { 'open': isNavbarOpen }]">
          <li><a class="nav__link" href="#home">Bosh Sahifa</a></li>
          <li><a class="nav__link" href="#About">Men haqimda</a></li>
          <li><a class="nav__link" href="#Diograma">Ko'nikmalar</a></li>
          <li><a class="nav__link" href="#connection">Bog'lanish</a></li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isNavbarOpen: false,
        isScrolled: false,  // Scroll holatini kuzatish
      };
    },
    methods: {
      toggleNavbar() {
        this.isNavbarOpen = !this.isNavbarOpen;
      },
      handleScroll() {
        this.isScrolled = window.scrollY > 50; // 50px pastga tushganda navbar rangini o'zgartirish
      },
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll); // scrollni kuzatish
    },
    beforeDestroy() {
      window.removeEventListener('scroll', this.handleScroll); // scrollni to'xtatish
    }
  };
  </script>
  
  <style scoped>
  .nav__container {
    height: 65px;
    color: white;
    background-color: blue;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    position: sticky;
    top: 0; /* Sahifa pastga tushganda navbar yuqorida turadi */
    z-index: 1000; /* Navbarni yuqori qatorda qilish uchun */
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
  }
  
  .nav__container.scrolled {
    background-color: darkblue; /* Scroll qilinganda navbar rangini o'zgartirish */
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Scroll qilinganda soyani qo'shish */
  }
  
  .left__nav {
    display: flex;
    align-items: center;
    font-size: 24px;
    width: 100%;
    justify-content: space-between;
  }
  
  .menu {
    display: flex;
    align-items: center;
    list-style-type: none;
    gap: 40px;
    margin: 0;
    padding: 0;
  }
  
  .nav__link {
    color: white;
    transition: 0.3s;
    text-decoration: none;
  }
  
  .nav__link:hover {
    color: black;
  }
  
  .toggle-button {
    font-size: 1.5rem;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
    display: none;
  }
  
  @media (max-width: 768px) {
    .menu {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 65px;
      left: 0;
      width: 100%;
      background-color: blue;
      padding: 10px 0;
      z-index: 10;
      transition: max-height 0.3s ease;
    }
  
    .menu.open {
      display: flex;
    }
  
    .toggle-button {
      display: block;
      position: absolute;
      right: 20px;
      top: 20px;
    }
  
    .nav__container {
      justify-content: flex-start;
      padding: 0 10px;
    }
  
    .nav__link {
      padding: 10px 20px;
      text-align: center;
      width: 100%;
      color: white;
      text-decoration: none;
    }
  }
  </style>
   
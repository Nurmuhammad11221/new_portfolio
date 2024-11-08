<template>
    <div class="nav__container">
      <!-- Mobil versiya uchun menyuni ochuvchi/yopuvchi tugma -->
      <button class="toggle-button" @click="toggleNavbar">
        ☰
      </button>
  
      <div class="left__nav">
        <h1>FINEDEV.uz</h1>
  
        <!-- Mobil va desktop versiyada ko'rinishi har xil bo'ladigan menyu -->
        <div :class="['menu', { 'open': isNavbarOpen }]">
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
            <a class="nav__link" href="">Bog'lanish</a>
          </li>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
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
  .nav__container {
    height: 65px;
    color: white;
    background-color: blue;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
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
    display: none; /* Mobilda ko'rinadi */
  }
  
  /* Mobil versiya uchun media query */
  @media (max-width: 768px) {
    .menu {
      display: none; /* Default ko'rinmaydi */
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
      display: flex; /* Tugma bosilganda ko'rinadi */
    }
  
    .toggle-button {
      display: block; /* Mobilda ko'rinadi */
      position: absolute;
      right: 20px; /* O'ng tomonda bo'lishi uchun */
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
  
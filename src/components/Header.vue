<template>
    <div class="container">
      <div class="header__title">
        <h1 class="title">
          Abdugafforov Nurmuhammad
        </h1><br><br>
        <p class="text">Developer</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    
  };
  </script>
  
  <style scoped>
  .container {
    height: 89vh;
    background-image: url('@/assets/1.1.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .header__title {
    text-align: center;
  }
  
  .title {
    color: white;
    font-size: 3rem; /* Desktopda kattaroq yoziladi */
  }
  
  .text {
    font-size: 20px;
    color: aliceblue;
  }
  
  /* Mobil versiya uchun media query */
  @media (max-width: 768px) {
    .title {
      font-size: 2rem; /* Mobilda kichikroq font */
    }
  
    .text {
      font-size: 16px; /* Mobilda kichikroq font */
    }
  }
  </style>
  
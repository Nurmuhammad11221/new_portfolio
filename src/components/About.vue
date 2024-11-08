<template>
    <div class="about__container">
      <div class="title">
        <div class="about__title">
          <h1>MEN HAQIMDA</h1>
        </div>
      </div>
  
      <div class="about">
        <div class="about__right">
          <button class="about__link">
            <a class="about__link-item" target="_blank" href="https://docs.google.com/document/d/1qEWYBKG9d3wANEyCSJWEdT9gEKaQNGJ5mTuVim7I_FE/edit?tab=t.0">RESUME</a>
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    
  }
  </script>
  
  <style scoped>
  .about__container {
    margin-top: 50px;
    height: 250px;
  }
  
  .about__title {
    text-align: center;
    color: blue;
  }
  
  .about__link {
    height: 60px;
    width: 100px;
    background-color: blue;
    border-radius: 15px;
    margin-top: 20px;
    transition: 0.8s;
  }
  
  .about__link-item {
    color: white;
    text-decoration: none;
    display: block;
    height: 100%;
    text-align: center;
    line-height: 60px; /* Vertikal o'rtalash */
  }
  
  .about__link:hover {
    background-color: black;
    box-shadow: 5px 5px 10px 10px;
  }
  
  .about {
    display: flex;
    justify-content: center; /* Mobil uchun markazga joylashtirish */
    align-items: center;
    margin-top: 10px;
  }
  
  /* Mobil versiya uchun media query */
  @media (max-width: 768px) {
    .about__container {
      height: auto; /* Ekran balandligiga moslashish */
      padding: 20px;
    }
  
    .about__title h1 {
      font-size: 1.5rem; /* Mobilda kichikroq font */
    }
  
    .about__link {
      width: 150px; /* Kattaroq tugma */
      height: 50px; /* Kichikroq bo'ladi */
      margin-top: 20px;
    }
  
    .about__link-item {
      font-size: 14px; /* Link uchun kichikroq yozuv */
    }
  
    .about {
      flex-direction: column; /* Tugmani pastga tushirish */
    }
  }
  </style>
  
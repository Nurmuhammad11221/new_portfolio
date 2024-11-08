<template>
    <div class="container">
      <div class="main__top">
        <h1 class="main__title">Bog'lanish</h1>
      </div>
  
      <div class="main__bottom">
        <div class="main__bottom-right">
          <a class="main__link" href="https://yandex.uz/maps/10335/tashkent/?ll=69.279737%2C41.311151&z=12">
            <img class="main__bottom-img" :src="require('@/assets/1.3.svg')" alt="Rasm tavsifi" />
            <p class="main__text">Toshkent shahri</p>
          </a>
        </div>
  
        <div class="main__bottom-center">
          <img class="main__bottom-img" :src="require('@/assets/1.4.svg')" alt="Rasm tavsifi" />
        </div>
  
        <div class="main__bottom-left">
          <img class="main__bottom-img" :src="require('@/assets/1.5.svg')" alt="Rasm tavsifi" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {}
  </script>
  
  <style>
    .main__title {
      text-align: center;
      color: blue;
      font-size: 38px;
    }
  
    .main__bottom {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 100px;
      gap: 34px;
    }
  
    /* Kartochkalarni markazlash */
    .main__bottom-right, .main__bottom-center, .main__bottom-left {
      width: 240px;
      height: 215px;
      box-shadow: 10px 1px 30px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      transition: transform 0.3s ease; /* Animatsiya o'tish */
    }
  
    /* Hover effekti - ikonka ustiga olib borilganda */
    .main__bottom-img:hover {
      transform: scale(1.2) translateY(-5px); /* Kattalashadi va yuqoriga ko'tariladi */
    }
  
    /* Icon va matn uslublari */
    .main__bottom-img {
      width: 50px;
      height: 50px;
      margin-bottom: 10px;
      transition: transform 0.3s ease; /* Animatsiya o'tish */
    }
  
    .main__text {
      margin-top: 10px;
      color: purple;
    }
  
    /* Mobil versiya uchun media query */
    @media (max-width: 768px) {
      .main__bottom {
        display: block;
      }
  
      .main__bottom-right, .main__bottom-center, .main__bottom-left {
        width: 100%;
        margin-bottom: 20px;
      }
  
      /* Mobil qurilmada hover effektini olib tashlash */
      .main__bottom-img:hover {
        transform: none; /* Hover effekti yo'q bo'ladi */
      }
    }
  </style>
  
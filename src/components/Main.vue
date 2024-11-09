<template>
  <div id="connection" class="main__container">
    <div class="main__top">
      <h1 class="main__title">Bog'lanish</h1>
    </div>

    <div class="main__bottom">
      <div class="main__bottom-right">
        <a class="main__link" target="_blank" href="https://yandex.uz/maps/10335/tashkent/?ll=69.279737%2C41.311151&z=12">
          <img class="main__bottom-img" :src="require('@/assets/1.3.svg')" alt="Rasm tavsifi" />
          <p class="main__text">Toshkent shahri</p>
        </a>
      </div>

      <div class="main__bottom-center">
        <img class="main__bottom-img" :src="require('@/assets/1.4.svg')" alt="Rasm tavsifi" />
        <p>+998917987700</p>
      </div>

      <div class="main__bottom-left">
        <a target="_blank" href="https://t.me/Anf_707">
          <img class="main__bottom-img" :src="require('@/assets/1.5.svg')" alt="Rasm tavsifi" /><br>707
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
  .main__container {
      padding: 20px;
  }
  
  .main__title {
      text-align: center;
      color: blue;
      font-size: 38px;
  }

  .main__bottom {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 34px;
      margin-top: 50px;
  }

  .main__bottom-right, .main__bottom-center, .main__bottom-left {
      width: 240px;
      height: 215px;
      box-shadow: 10px 1px 30px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      transition: transform 0.3s ease;
      background-color: white; 
  }

  .main__bottom-img:hover {
      transform: scale(1.2) translateY(-5px); 
  }

  .main__bottom-img {
      width: 50px;
      height: 50px;
      margin-bottom: 10px;
      transition: transform 0.3s ease;
  }

  .main__text {
      margin-top: 10px;
      color: purple;
  }

  @media (max-width: 768px) {
      .main__bottom {
          display: block;
      }

      .main__bottom-right, .main__bottom-center, .main__bottom-left {
          width: 100%;
          margin-bottom: 20px;
      }

      .main__bottom-img:hover {
          transform: none;
      }
  }
</style>

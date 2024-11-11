<template>
    <div id="Diograma" class="section__container">
      <div class="section__top">
        <div class="section__title">
          <h1>KO'NIKMALAR</h1>
        </div>
      </div>
  
      <div class="section__buttom">
        <div class="section__left">
          <h2 class="section__title-item">Mening ko'nikmalarim va tajribalarim</h2>
          <p class="section__text">
            HTML, CSS, JavaScript, Python, Django, Vue, React va SQL kabi texnologiyalarni mukammal egallaganman. <br>
            HTML yordamida veb-sahifalar yaratishni, CSS bilan ularga estetik dizayn berishni, JavaScript orqali sahifalarga <br>
            dinamiklik qo'shishni va foydalanuvchilar bilan interaktiv aloqani ta'minlashni yaxshi bilaman. MySQL ma'lumotlar <br>
            bazasida ma'lumotlarni samarali saqlash va ularga tezkor so'rovlar yuborishni ham bajaraman. Ushbu texnologiyalar <br>
            bilan turli veb-loyihalar yaratib, o'z malakamni doimiy ravishda oshirib boryapman.
          </p>
        </div>
  
        <div class="section__right">
          <div v-for="(skill, index) in skills" :key="index" class="section__right-dg">
            <h4>{{ skill.name }}</h4>
            <h4>{{ skill.percentage }}%</h4>
            <div class="progress-bar-container">
              <div 
                :style="{
                  width: skill.percentage + '%', 
                  backgroundColor: skill.color, 
                  animationDuration: '2s',
                  animationName: 'progress-animation-' + skill.name
                }" 
                class="progress-bar-fill"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        skills: [
          { name: 'HTML', percentage: 95, color: '#ff7043' },
          { name: 'CSS', percentage: 85, color: '#42a5f5' },   
          { name: 'Python', percentage: 70, color: '#66bb6a' }, 
          { name: 'Django', percentage: 45, color: '#ffca28' }  
        ]
      };
    }
  };
  </script>
  
  <style>
  .section__container {
    height: 600px;
    font-family: 'Arial', sans-serif;
  }
  
  .section__title {
    text-align: center;
    color: #2e3b4e; 
  }
  
  .section__top h1 {
    font-size: 2.5em;
    letter-spacing: 1px;
    margin: 0;
  }
  
  .section__buttom {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-top: 50px;
    gap: 30px;
  }
  
  .section__left {
    width: 45%;
    text-align: center;
    padding: 0 20px;
  }
  
  .section__title-item {
    color: #4d90fe; 
    font-size: 1.8em;
  }
  
  .section__text {
    color: #4f4f4f; 
    line-height: 1.8;
    font-size: 1.1em;
    margin-top: 20px;
  }
  
  .section__right {
    width: 45%;
  }
  
  .progress-bar-container {
    width: 100%;
    height: 20px;
    background-color: #e0e0e0; 
    border-radius: 10px;
    overflow: hidden;
    margin-bottom: 15px;
  }
  
  @keyframes progress-animation-HTML {
    0% {
      width: 0%;
    }
    100% {
      width: 95%;
    }
  }
  
  @keyframes progress-animation-CSS {
    0% {
      width: 0%;
    }
    100% {
      width: 85%;
    }
  }
  
  @keyframes progress-animation-Python {
    0% {
      width: 0%;
    }
    100% {
      width: 70%;
    }
  }
  
  @keyframes progress-animation-Django {
    0% {
      width: 0%;
    }
    100% {
      width: 45%;
    }
  }
  
  /* Applying the Animation */
  .progress-bar-fill {
    height: 100%;
    border-radius: 10px;
    animation-timing-function: ease-in-out;
    animation-duration: 2s;
    animation-fill-mode: forwards;
  }
  
  .progress-bar-fill:nth-child(1) {
    background-color: #ff7043; 
  }
  
  .progress-bar-fill:nth-child(2) {
    background-color: #42a5f5; 
  }
  
  .progress-bar-fill:nth-child(3) {
    background-color: #66bb6a; 
  }
  
  .progress-bar-fill:nth-child(4) {
    background-color: #ffca28; 
  }
  
  /* Responsive Styles */
  @media (max-width: 768px) {
    .section__buttom {
      flex-direction: column;
      gap: 20px;
      margin-top: 20px;
    }
  
    .section__left {
      width: 100%;
      text-align: center;
      padding: 0 20px;
    }
  
    .section__title-item {
      font-size: 1.5em;
    }
  
    .section__text {
      font-size: 1em;
      line-height: 1.6;
    }
  }
  
  @media (max-width: 480px) {
    .section__title h1 {
      font-size: 1.5em;
    }
  
    .section__left {
      padding: 0 10px;
    }
  
    .section__title-item {
      font-size: 1.2em;
    }
  
    .section__text {
      font-size: 0.9em;
    }
  }
  </style>


  
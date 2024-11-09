<template>
    <div id="About" class="about__container">
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
    height: 200px;
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
    line-height: 60px; 
  }
  
  .about__link:hover {
    background-color: black;
    box-shadow: 5px 5px 10px 10px;
  }
  
  .about {
    display: flex;
    justify-content: center; 
    align-items: center;
    margin-top: 10px;
  }
  
  @media (max-width: 768px) {
    .about__container {
      height: auto; 
      padding: 20px;
    }
  
    .about__title h1 {
      font-size: 1.5rem; 
    }
  
    .about__link {
      width: 150px; 
      height: 50px; 
      margin-top: 20px;
    }
  
    .about__link-item {
      font-size: 14px; 
    }
  
    .about {
      flex-direction: column;
    }
  }
  </style>
  
<template>
    <div class="blog__container">
        <div class="blog__left">
            <p class="blog__text">
                I'm 14 years old, I'm currently working in Front end,<br> I'm currently working in "Fayz Talim" educational center,<br> it's very good, I've been going there for 4 months now,<br> I know HTML, CSS, BOOTSTRAP,Python,Django languages ,<br>I'm currently running vue.js and I'm also running this site on vue. <br><br> <a class="blog__link" href="https://docs.google.com/document/d/1qEWYBKG9d3wANEyCSJWEdT9gEKaQNGJ5mTuVim7I_FE/edit?tab=t.0#heading=h.f1fzwhzuftn"> Additional Information</a>
                </p>
        </div>
        <div class="blog__right"></div>
    </div>
</template>

<script>
export default {

}
</script>

<style>

.blog__container {
    height: 89vh;
    background-image: url('@/assets/1.6.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 40px;
  }



  .blog__left{
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        display: flex;
        justify-content: start;
        align-content: center; 
        font-weight: bold;
        color: rgb(51, 0, 253);

  }

  .blog__link{
    color: aliceblue ;
  }
</style>
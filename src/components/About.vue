<template>
    <div class="about__container">
        <div class="title">
            <div class="about__title">
                <h1>MEN HAQIMDA</h1>
            </div>

        </div>

        <div class="about">

                
            <div class="about__right">
                <button class="about__link"><a class="about__link-item" href="https://docs.google.com/document/d/1qEWYBKG9d3wANEyCSJWEdT9gEKaQNGJ5mTuVim7I_FE/edit?tab=t.0">RESUME</a></button>
            </div>

        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    .about__container{
        margin-top: 50px;
        height: 200px;

    }
    .about__title{
        text-align: center  ;
        color: blue;
        
        
    }

    .about__link{
        height: 60px;
        width: 100px;
        background-color: blue;
        border-radius: 15px;
        margin-top: 20px;


        transition: 0.8s;
    }
    .about__link-item{
        color: white;
    }
    .about__link:hover{
        background-color: black;
    }
    .about{
        display: flex;
        justify-content: space-around;
        align-items: center;
        margin-top: 10px;
    }

    .about__right{

    }

</style>
<template>
    <section>
        <h2>Отзывы</h2>
        <ReviewSlider/>
    </section>
</template>

<script>
import ReviewSlider from "./ReviewSlider.vue";
export default{
    components:{
        ReviewSlider
    }
}

</script>

<style scoped>
section{
    margin-bottom: 160px;
    font-family: Montserrat;
    font-style: normal;
    background: url(../assets/themes/right-quote-sign.svg) no-repeat left top;
    background-size: 26%;
    padding-top: 90px;
}
h2{
    font-family: Montserrat;
    font-weight: bold;
    font-size: 42px;
    text-align: center;
    color: #050c33;
    margin-bottom:46px;
}
a:hover{
    color: #050c33;
}
@media (min-width: 1400px){
    .container {
        max-width: 1140px;
    }
}
@media (max-width: 1080px){
    h2{
        font-size: 36px;
    }
}
@media (max-width: 991px){
    h2{
        margin-top: 20px;
        font-size: 32px;
    }
}
@media (max-width: 767px){
    h2{
        font-size: 24px;
        margin-bottom: 20px;
        margin-top: initial;
    }
    .container{
        max-width: 767px;
    }
}
</style>
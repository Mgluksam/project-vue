<template>
    <section class="container m-auto">
        <h2>Последние кейсы</h2>
        <div class="cases">
            <CaseCard v-for="cs in cases" :cs="cs"/>
        </div>
        <div class="more-btn">
            <a href="">Показать еще</a>
        </div>
    </section>
</template>

<script>
import cases from '../data/cases.json';
import CaseCard  from './CaseCard.vue';
export default{
    data(){
        return{
          cases  
        } 
    },
    components:{
        CaseCard
    }
}
</script>

<style scoped>
.container{
    margin-top: 100px;
}
h2{
    font-family: Montserrat;
    font-weight: bold;
    font-size: 42px;
    text-align: center;
    color: #050c33;
    margin-bottom: 80px;
    margin-top: 130px;
}
.cases{
    display: flex;
    flex-wrap: wrap;
    text-align: left;
    font-family: Montserrat;
}
a{
    display: inline-block;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 1;
    text-transform: uppercase;
    color: #050c33;
    padding: 24px 75px;
    border: 1px solid #cccdd5;
    border-radius: 5px;
    text-decoration: none;
    margin-bottom: 20px;
}
a:hover{
    color: #050c33;
}
.more-btn{
    text-align: center;
    margin-bottom: 30px;
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
    a{
        padding: 10px 30px;
    }
    h2{
        margin-top: 20px;
    }
}
@media (max-width: 767px){
    h2{
        font-size: 24px;
        margin-bottom: 20px;
        margin-top: initial;
    }
    .container{
        padding-top: 50px;
        max-width: 767px;
    }
}
</style>
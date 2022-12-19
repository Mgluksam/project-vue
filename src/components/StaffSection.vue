<template>
    <section class="container m-auto">
        <h2>Команда</h2>
        <div class="team">
            <StaffCard v-for="l in ls" :imgSrc="l.image" :Name="l.name" :post="l.post"/>
        </div>
    </section>
</template>

<script>
import ls from '../data/staff.json';
import StaffCard from './StaffCard.vue';
export default{
    data(){
        return{
          ls  
        } 
    },
    components:{
        StaffCard
    }
}
</script>

<style scoped>
@media (min-width: 1400px){
.container {
    max-width: 1140px;
}
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
.team{
    display: flex;
    flex-wrap: wrap;
    text-align: left;
    font-family: Montserrat;
}
</style>
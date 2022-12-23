<template>
  <HeaderVue/>
  <Competencies/>
  <Advantages/>
</template>

<script>
import HeaderVue from './components/Header.vue';
import StaffSection from './components/StaffSection.vue';
import LastCasesSection from './components/LastCasesSection.vue';
import ReviewsSection from './components/ReviewsSection.vue';
import Competencies from './components/Competencies.vue';
import Advantages from './components/Advantages.vue';
export default{
  components:{
    HeaderVue,
    StaffSection,
    LastCasesSection,
    ReviewsSection,
    Competencies,
    Advantages
}
}
</script>

<style>

</style>

<template>
  <LastCasesSection/>
  <StaffSection/>
  <ReviewsSection/>

</template>

<script>
import HeaderVue from './components/Header.vue';
import StaffSection from './components/StaffSection.vue';
import LastCasesSection from './components/LastCasesSection.vue';
import ReviewsSection from './components/ReviewsSection.vue';
export default{
  components:{
    HeaderVue,
    StaffSection,
    LastCasesSection,
    ReviewsSection
}
}
</script>

<style>

</style>

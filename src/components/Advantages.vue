<template>
  <div class="advantages with-expertise">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2 class="block-title">
            Поддержка <br />
            от Drupal-coder
          </h2>
        </div>
      </div>
      <div class="row row-flex advantages-row">
        <AdvantagesCard v-for="i in info" :id="i.id" :imgSrc="i.image" :titleText="i.titleText" :bodyText="i.bodyText"/>
      </div>
    </div>
  </div>
</template>

<script>
import AdvantagesCard from "./AdvantagesCard.vue";
import info from "../data/advantages.json";
export default {
  data() {
    return {
      info,
    };
  },
  components: {
    AdvantagesCard,
  },
};
</script>

<style scoped>
.advantages {
  font-family: Montserrat;
}
.advantages h2 {
  margin-bottom: 55px;
  text-align: center;
  color: #050c33;
  font-weight: bold;
  font-size: 42px;
}

.advantages-row {
  padding: 0 12px;
  position: relative;
  z-index: 20;
}
.row-flex {
    display: flex;
    flex-wrap: wrap;
    margin-bottom: 75px;
}

.with-expertise .advantages-row {
  margin-bottom: -212px;
}
</style>

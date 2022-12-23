<template>
  <div class="competencies">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <h2 class="block-title">
            17 лет совершенствуем <br />
            компетенции в Drupal <br />
            разработке!
          </h2>
          <div class="competencies-description">
            Разрабатываем и оптимизируем модули, расширяем <br />
            функциональность сайтов, обновляем дизайн
          </div>
        </div>
      </div>
      <div class="row row-flex competencies-row">
        <OneCompetency v-for="i in info" :imgSrc="i.image" :text="i.text"/>
      </div>
    </div>
  </div>
</template>

<script>
import OneCompetency from "./OneCompetency.vue";
import info from "../data/competencies.json";
export default {
  data() {
    return {
      info
    };
  },
  components: {
    OneCompetency
  },
};
</script>

<style scoped>
.competencies {
  padding: 100px 0;
  font-family: Montserrat;
}
.competencies h2 {
  font-weight: bold;
  font-size: 42px;
  color: #050c33;
  margin: 0 0 20px;
}
.competencies-description {
  margin-bottom: 55px;
  font-weight: 500;
  font-size: 16px;
  color: #4f5a73;
}

.row-flex {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 75px;
}
.competencies-row {
  margin-bottom: 0;
}
</style>

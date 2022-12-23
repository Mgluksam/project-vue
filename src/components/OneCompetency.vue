<template>
  <div class="col-sm-3 col-xs-6">
    <div class="competency">
      <div class="competency-wrapper">
        <div class="competency-header">
          <div class="competency-icon">
            <img
              :src="require('@/' + imgSrc)"
              width="81"
              height="81"
              class="img-responsive"
            />
          </div>
        </div>
        <div class="competency-body">
          {{ text }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imgSrc: String,
    text: String,
  }
};
</script>

<style scoped>
.competency {
  margin-bottom: 60px;
}
.competency-body {
  font-weight: 500;
  font-size: 16px;
  color: #4f5a73;
}
.competency-icon {
  position: relative;
  margin-bottom: 30px;
}
.img-responsive {
  display: block;
  max-width: 100%;
  height: auto;
}
</style>

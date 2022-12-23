<template>
  <div class="col-sm-6 col-md-3 col-xs-12 advantage-col">
    <div class="advantage">
      <div class="advantage-wrapper">
        <div class="advantage-header">
          <div class="advantage-num" v-html="id"></div>
          <div class="advantage-title" v-html="titleText">
          </div>
        </div>
        <div class="advantage-body" v-html="bodyText">
        </div>
        <div class="advantage-icon">
          <img
            :src="require('@/' + imgSrc)"
            class="img-responsive"
            loading="lazy"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    imgSrc: String,
    titleText: String,
    bodyText: String
  },
};
</script>

<style scoped>
.advantage-col {
  margin-bottom: 5px;
  padding: 0px 15px;
}
.advantage {
  background: #fff;
  border-radius: 5px;
  box-shadow: 20px 20px 40px rgb(5 12 51 / 5%);
  margin-left: -12px;
  margin-right: -12px;
  height: 100%;
  position: relative;
  padding: 25px 25px 45px;
  min-height: 292px;
}
.advantage-body {
  position: relative;
  z-index: 10;
  font-weight: 500;
  font-size: 16px;
  color: #4e5a73;
  line-height: 1.37;
}
.advantage-icon {
  position: absolute;
  right: 0;
  bottom: 0;
  z-index: 5;
}
.advantage-num {
  font-weight: bold;
  font-size: 12px;
  color: #828a9b;
  margin-bottom: 20px;
}
.advantage-title {
  font-weight: bold;
  font-size: 18px;
  color: #050c33;
  line-height: 1.22;
  margin-bottom: 15px;
}
.img-responsive {
  display: block;
  max-width: 100%;
  height: auto;
}
</style>

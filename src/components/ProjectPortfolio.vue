<template>
  <div
    @mouseenter="showHoveredCard"
    @mouseleave="hideHoveredCard"
    class="project-portfolio"
  >
    <img class="project-img" :src="src" />
    <div class="project-show" v-if="isCardShown">
      <img class="project-img-inside" :src="src" />
      <div class="project-info">
        <div class="project-date">
          {{ date }}
        </div>
        <div class="project-title">
          {{ title }}
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ProjectPortfolio",
  data() {
    return {
      isCardShown: false,
    };
  },
  props: {
    src: String,
    date: String,
    title: String,
    index: Number
  },
  methods: {
    showHoveredCard() {
      this.isCardShown = true;
    },
    hideHoveredCard() {
      this.isCardShown = false;
    },
  },
};
</script>
<style scoped>
.project-portfolio {
  width: 33.33%;
  height: 300px;
  position: relative;
}
.project-img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}
.project-img-inside {
  object-fit: cover;
  width: 100%;
  height: 225px;
}
.project-info {
  height: 115px;
  background: #3B43F2;
  color: white;
  text-align: left;
  padding: 16px 32px;
}
.project-title {
  font-size: 32px;
  margin-top: 8px;
}
.project-show {
  position: absolute;
  height: 340px;
  width: 105%;
  z-index: 2;
  top: 50%;
  bottom: 50%;
  transform: translate(-2%, -50%);
  box-shadow: 0px 20px 80px rgba(0, 0, 0, 0.2);
}
</style>

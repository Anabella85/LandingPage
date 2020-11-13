<template>
  <div class="expertise">
    <img :src="src" />
    <div class="expertise-title">
      {{ title }}
    </div>
    <div class="expertise-description">
      {{ description }}
    </div>
  </div>
</template>
<script>
export default {
  name: "ExpertiseCard",
  data() {
    return {};
  },
  props: {
    src: String,
    title: String,
    description: String,
  },
};
</script>
<style scoped>
.expertise {
  width: 300px;
  height: 350px;
  border-radius: 18px;
  padding: 32px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transition: .5s;
  margin-top: 20px;
}
.expertise:hover {
  background: #FFFFFF;
  border: 1px solid #D8D8D8;
  box-shadow: 0px 20px 80px rgba(0, 0, 0, 0.15);
  background: white;
  margin-top: 0px;
}
.expertise-title {
  font-style: normal;
  font-weight: 500;
  font-size: 24px;
  line-height: 32px;
  text-align: center;
  color: #222A41;
  margin: 24px 0;
}
.expertise-description {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 28px;
  text-align: center;
  color: #6D7783;
}
</style>
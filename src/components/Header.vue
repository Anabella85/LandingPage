<template>
  <div class="container container-header">
    <div class="container-menu">
      <div class="logo">
        <img src="../assets/header-logo.svg" />
      </div>
      <div class="header-btn">
        <a href="#about"><div class="content-btn">About</div></a>
        <a href="#portfolio"><div class="content-btn">Portfolio</div></a>
        <a href="#contact"><div class="content-btn">Contact</div> </a>
      </div>
    </div>

    <div class="header-social-btn">
      <a href="http://www.facebook.com" target="__blank"
        ><img src="../assets/header-fb.svg"
      /></a>
      <a href="https://www.instagram.com" target="__blank"
        ><img src="../assets/header-insta.svg"
      /></a>
      <a href="http://www.twitter.com" target="__blank"
        ><img src="../assets/header-twitter.svg"
      /></a>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header",
};
</script>
<style scoped>
.container-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 16px;
}
.container-menu {
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo {
  height: 55px;
  width: 55px;
  margin-right: 60px;
}
.header-btn {
  font-size: 16px;
  line-height: 24px;
  color: rgba(34, 42, 65, 1);
  display: flex;
  justify-content: space-between;
}
.header-btn a {
  color: #222A41;
  margin-right: 32px;
  text-decoration: none;
}
.header-social-btn {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
}
.header-social-btn a {
  color: #DBDBDB;
  margin-left: 16px;
}
</style>
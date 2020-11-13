<template>
    <div class="container">
        <div class="content">
            <a href="../About.vue"><div class="content-btn">Home</div></a>
            <a href="#about"><div class="content-btn">About </div></a>
            <a href="#portfolio"><div class="content-btn">Portfolio</div></a>
            <a href="#contact"><div class="content-btn"> Contact</div> </a>                       
        </div>
        <div class="social-btn">
            <a href="http://www.facebook.com"><img src="../assets/fb-btn.svg"></a>
            <a href="https://www.instagram.com"><img src="../assets/insta-btn.svg"></a>
            <a href="http://www.twitter.com"><img src="../assets/twitter.svg"></a>
        </div>
        <div class="copyright">Design with love © Tanahcon 2019. All right reserved</div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.content{
    margin: 60px auto 30px auto;
    height:24px;
    width:329px;
    display:flex;
    justify-content: space-between;
}
.content-btn{
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    text-align: center;
    color: #222A41;
}
.social-btn{
    width: 146px;
    height: 40px;
    display:flex;
    justify-content: space-between;
    margin:auto;
    margin-bottom:30px;
}
.copyright{
    font-style: normal;
    font-weight: normal;
    font-size: 13px;
    line-height: 16px;
    text-align: center;
    color: #6D7783;
    margin-bottom:60px;
}
</style>
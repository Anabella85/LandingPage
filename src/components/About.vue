<template>
  <div class="container">
    <img class="background-about" src="../assets/background-about.svg" />
    <div class="hero">
      <div class="hero-text">
        <div class="header-small-text">Hello</div>
        <div class="header-big-text">I’m Orion</div>
        <div class="description">
          Freelance UI/UX Designer, also passionate in making beautiful
          illustrations and icons
        </div>
        <button class="btn btn-action" :click="hireMe">Hire me</button>
      </div>
      <img class="oval" src="../assets/dog8.jpg" />
    </div>
    <div class="hero hero-margin">
      <img class="square" src="../assets/dog8.jpg" />
      <div id="about" class="hero-text">
        <div class="header-small-text">A bit</div>
        <div class="header-big-text">About me</div>
        <div class="category">
          <b-tabs
            active-nav-item-class="active-class"
            no-nav-style
            content-class="mt-3"
          >
            <b-tab
              v-for="(info, index) in aboutMeInfo"
              :key="index"
              :title="info.title"
              title-link-class="link-class"
            >
              <div class="description">
                {{ info.description }}
              </div>
            </b-tab>
          </b-tabs>
        </div>
        <button class="btn btn-action">Download CV</button>
      </div>
    </div>
    <div class="elipse"></div>
    <div class="expertise">
      <div class="hero margin-expertise">
        <div class="hero-text-align">
          <div class="header-small-text">Skills</div>
          <div class="header-big-text">Expertise</div>
          <div class="description">
            Freelance UI/UX Designer, also passionate in making beautiful
            illustrations and icons
          </div>
        </div>
      </div>
      <div class="skills">
        <ExpertiseCard
          v-for="(skill, index) in skills"
          :key="index"
          :title="skill.title"
          :description="skill.description"
          :src="skill.src"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ExpertiseCard from "./ExpertiseCard";
import skill1 from "../assets/skill1.svg";
import skill2 from "../assets/skill2.svg";
import skill3 from "../assets/skill3.svg";
export default {
  name: "About",
  components: {
    ExpertiseCard,
  },
  data() {
    return {
      skills: [
        {
          src: skill1,
          title: "UI/UX Design",
          description:
            "Launch party pitch technology user experience innovator buzz stealth MVP business model.",
        },
        {
          src: skill2,
          title: "Local SEO",
          description:
            "Launch party pitch technology user experience innovator buzz stealth MVP business model.",
        },
        {
          src: skill3,
          title: "Social Media Marketing",
          description:
            "Launch party pitch technology user experience innovator buzz stealth MVP business model.",
        },
      ],
      aboutMeInfo: [
        {
          title: "Life",
          description:
            "Pacific housing unique experiences things to do motel nature flexibility international bus place to stay miles kayak overnight territory. Chartering dollar nighttrain city trip. Cuba caravan Brasil Australia guide place to stay horse riding camper Budapest.",
        },
        {
          title: "Education",
          description:
            "Pacific housing unique experiences things to do motel nature flexibility international bus place to stay miles kayak overnight territory. Chartering dollar nighttrain city trip. Cuba caravan Brasil Australia guide place to stay horse riding camper Budapest.",
        },
        {
          title: "Experience",
          description:
            "Pacific housing unique experiences things to do motel nature flexibility international bus place to stay miles kayak overnight territory. Chartering dollar nighttrain city trip. Cuba caravan Brasil Australia guide place to stay horse riding camper Budapest.",
        },
      ],
    };
  },
  methods: {
    hireMe() {
      console.log("test");
    },
  },
};
</script>

<style>
.active-class {
  border-bottom: 2px solid #3138D1;
}
.link-class {
  color: #293340;
}
</style>

<style scoped>
.background-about {
  position: absolute;
  left: 0px;
  top: 771px;
  z-index: -1;
}
.container {
  margin-bottom: 60px;
}
.hero {
  flex-direction: row;
  display: flex;
  width: 85%;
  margin: auto;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 250px;
}
.hero-margin {
  margin-bottom: 80px;
}
.margin-expertise {
  margin-bottom: 0px;
}
.hero-text {
  width: 332px;
  text-align: left;
  margin-top: 235px;
}
.hero-text-align {
  width: 332px;
  text-align: center;
  display: flex;
  align-items: center;
  flex-direction: column;
  margin: auto;
  margin-top: 91px;
}
.header-small-text {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 27px;
  color: #222A41;
  margin-bottom: 11px;
}
.header-big-text {
  font-style: normal;
  font-weight: bold;
  font-size: 60px;
  line-height: 80px;
  color: #222A41;
  margin-bottom: 9px;
}
.description {
  font-style: normal;
  font-weight: normal;
  font-size: 15px;
  line-height: 24px;
  color: #6D7783;
  margin-bottom: 30px;
}
.btn-action {
  height: 50px;
  width: 154px;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  color: #FFFFFF;
  background-color: rgb(42, 42, 219);
  border-radius: 25px;
  border: none;
}
.oval {
  background: #B4B4B4;
  box-shadow: 40px 2px 80px rgba(0, 0, 0, 0.5);
  border-radius: 50%;
  width: 360px;
  height: 360px;
  margin-top: 161px;
}
.square {
  width: 360px;
  height: 360px;
  background: #B4B4B4;
  box-shadow: -40px 2px 80px rgba(0, 0, 0, 0.5);
  border-radius: 18px;
}
.category {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 23px;
  color: #293340;
  margin-top: 30px;
  margin-bottom: 33px;
  border: none;
}
.elipse {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: #C4C4C4;
  margin-top: 24px;
  margin: auto;
}
.skills {
  display: flex;
  flex-flow: row;
  justify-content: space-between;
  margin-top: 60px;
  height: 350px;
}
</style>


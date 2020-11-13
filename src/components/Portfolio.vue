<template>
  <div class="container-portfolio">
    <div class="text">
      <div id="port" class="title">Selected Portfolio</div>
      <div class="description">
        Freelance UI/UX Designer, also passionate in making beautiful
        illustrations and icons
      </div>
      <div class="btn-container">
        <div>
          <button
            v-for="(button, index) in buttons"
            :key="index"
            @click="filterProjects(button.type)"
            class="btn button-design"
          >
            {{ button.text }}
          </button>
        </div>
        <button @click="filterProjects('all')" class="btn btn-action">
          View All
        </button>
      </div>
    </div>
      <div class="projects">
      <ProjectPortfolio
        v-for="(project, index) in filteredProjects"
        :key="index"
        :title="project.title"
        :date="project.date"
        :src="project.src"
      />
    </div>
  </div>
</template>
<script>
import ProjectPortfolio from "./ProjectPortfolio";
import dog from "../assets/dog.jpg";
import dog2 from "../assets/dog2.jpg";
import dog3 from "../assets/dog3.jpg";
import dog4 from "../assets/dog4.jpg";
import dog5 from "../assets/dog5.jpg";
import dog6 from "../assets/dog6.jpg";
import dog7 from "../assets/dog7.jpg";
import dog8 from "../assets/dog8.jpg";
import dog9 from "../assets/dog9.jpg";
export default {
  name: "Portfolio",
  components: {
    ProjectPortfolio,
  },
  data() {
    return {
      filteredProjects: [],
      buttons: [
        {
          text: "UI Design",
          type: "ui-design",
        },
        {
          text: "UX Design",
          type: "ux-design",
        },

        {
          text: "Graphic Design",
          type: "graphic-design",
        },
        {
          text: "Branding",
          type: "branding",
        },
        {
          text: "Icon",
          type: "icon",
        },
      ],
      projects: [
        {
          src: dog,
          date: "25 December 2019",
          title: "Website Project 1",
          type: "ui-design",
        },
        {
          src: dog2,
          date: "25 December 2019",
          title: "Lorem Ipsum Website Project",
          type: "ui-design",
        },
        {
          src: dog3,
          date: "25 April 2019",
          title: "Website Project 3",
          type: "ui-design",
        },
        {
          src: dog4,
          date: "25 May 2019",
          title: "Website Project 4",
          type: "ux-design",
        },
        {
          src: dog5,
          date: "25 June 2019",
          title: "Website Project 5",
          type: "graphic-design",
        },
        {
          src: dog6,
          date: "25 March 2019",
          title: "Website Project 6",
          type: "branding",
        },
        { 
          src: dog7, 
          date: "25 July 2019", 
          title: "Website Project 7", 
          type: "icon" 
        },
        {
          src: dog8,
          date: "25 September 2019",
          title: "Website Project 8",
          type: "ux-design",
        },
        { 
          src: dog9, 
          date: "25 August 2019", 
          title: "Website Project 9", 
          type: "icon" 
        },
      ],
    };
  },
  methods: {
    filterProjects(type) {
      if (type === "all") {
        this.filteredProjects = this.projects;
      } else {
        this.filteredProjects = this.projects.filter(
          (project) => project.type === type
        );
      }
    },
  },
  mounted() {
    this.filteredProjects = this.projects;
  },
};
</script>
<style scoped>
.container-portfolio {
  background-color: #3B43F2;
  overflow: hidden;
}
.text {
  width: 892px;
  height: 226px;
  text-align: left;
  margin: 150px auto;
}
.title {
  font-style: normal;
  font-weight: bold;
  font-size: 60px;
  line-height: 80px;
  letter-spacing: -1.76471px;
  color: #FFFFFF;
  margin-bottom: 18px;
  height: 80px;
  width: 485px;
}
.description {
  font-style: normal;
  font-weight: normal;
  font-size: 15px;
  line-height: 24px;
  color: #FFFFFF;
  margin-bottom: 30px;
  height: 48px;
  width: 332px;
}
.category {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 23px;
  color: #FFFFFF;
  display: flex;
  flex-flow: row;
  justify-content: space-between;
  margin-bottom: 10px;
}
.btn-action {
  height: 50px;
  width: 154px;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  color: #3B43F2;
  background: #FFFFFF;
  border: 1px solid #F2F2F2;
  border-radius: 25px;
}
.projects {
  display: flex;
  flex-flow: row wrap;
  background: white;
  border: 1px solid black;
  border-bottom: none;
  padding-bottom: 32px;
}
.button-design {
  background: transparent;
  color: white;
  font-size: 18px;
  border-radius: unset;
  height: 40px;
  box-shadow: none !important;
}
.button-design:hover {
  border-bottom: 2px solid white;
  color: white;
}
.btn-container {
  width: 100%;
  display: flex;
  justify-content: space-between;
}
</style>
<template>
  <div class="container">
    <img
      class="background-testimonial"
      src="../assets/background-testimonial.svg"
    />
    <div class="text">
      <div class="small-text">Clients</div>
      <div class="title">Some notable clients</div>
      <div class="description">
        Freelance UI/UX Designer, also passionate in making beautiful
        illustrations and icons
      </div>
    </div>

    <div class="clients">
      <img src="../assets/logo0.svg" />
      <img src="../assets/logo1.svg" />
      <img src="../assets/logo2.svg" />
      <img src="../assets/logo3.svg" />
      <img src="../assets/logo4.svg" />
    </div>
    <div
      id="carouselExampleCaptions"
      class="carousel slide"
      data-ride="carousel"
    >
      <ol class="carousel-indicators">
        <li
          data-target="#carouselExampleCaptions"
          data-slide-to="0"
          class="carousel-indicator"
        ></li>
        <li
          data-target="#carouselExampleCaptions"
          data-slide-to="1"
          class="carousel-indicator"
        ></li>
        <li
          data-target="#carouselExampleCaptions"
          data-slide-to="2"
          class="carousel-indicator active active-color"
        ></li>
        <li
          data-target="#carouselExampleCaptions"
          data-slide-to="3"
          class="carousel-indicator"
        ></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item">
          <div class="testimony">
            <img class="photo-person" src="../assets/dog2.jpg" />
            <div class="info-card">
              <div class="img"><img src="../assets/quote.svg" /></div>
              <div class="quote">
                “Lean startup metrics venture innovator assets angel investor
                learning curve incubator branding advisor termsheet. IPad
                ecosystem conversion android advisor. Incubator vesting period
                metrics crowdfunding backing interaction design business model
                canvas strategy”
              </div>
              <div class="person">Silvia Natalia</div>
              <div class="person function">Owner Tanahcon</div>
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="testimony">
            <img class="photo-person" src="../assets/dog2.jpg" />
            <div class="info-card">
              <div class="img"><img src="../assets/quote.svg" /></div>
              <div class="quote">
                “Lean startup metrics venture innovator assets angel investor
                learning curve incubator branding advisor termsheet. IPad
                ecosystem conversion android advisor. Incubator vesting period
                metrics crowdfunding backing interaction design business model
                canvas strategy”
              </div>
              <div class="person">Silvia Natalia</div>
              <div class="person function">Owner Tanahcon</div>
            </div>
          </div>
        </div>
        <div class="carousel-item active active-color">
          <div class="testimony">
            <img class="photo-person" src="../assets/dog2.jpg" />
            <div class="info-card">
              <div class="img"><img src="../assets/quote.svg" /></div>
              <div class="quote">
                “Lean startup metrics venture innovator assets angel investor
                learning curve incubator branding advisor termsheet. IPad
                ecosystem conversion android advisor. Incubator vesting period
                metrics crowdfunding backing interaction design business model
                canvas strategy”
              </div>
              <div class="person">Silvia Natalia</div>
              <div class="person function">Owner Tanahcon</div>
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="testimony">
            <img class="photo-person" src="../assets/dog2.jpg" />
            <div class="info-card">
              <div class="img"><img src="../assets/quote.svg" /></div>
              <div class="quote">
                “Lean startup metrics venture innovator assets angel investor
                learning curve incubator branding advisor termsheet. IPad
                ecosystem conversion android advisor. Incubator vesting period
                metrics crowdfunding backing interaction design business model
                canvas strategy”
              </div>
              <div class="person">Silvia Natalia</div>
              <div class="person function">Owner Tanahcon</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div id="contact" class="contact-form">
      <div class="infomessage">Fell free to contact me and say hello!</div>
      <div class="form">
        <b-form @submit="onSubmit" v-if="show">
          <b-form-group id="input-group-2" label-for="input-2">
            <b-form-input
              id="input-2"
              v-model="form.name"
              required
              placeholder="Your name"
              class="line"
            ></b-form-input>
          </b-form-group>
          <div class="bottom-line"></div>
          <b-form-group id="input-group-1" label-for="input-1">
            <b-form-input
              id="input-1"
              v-model="form.email"
              type="email"
              required
              placeholder="E-mail address"
              class="line"
            ></b-form-input>
          </b-form-group>
          <div class="bottom-line"></div>
          <b-form-group id="input-group-3" label-for="input-3">
            <b-form-textarea
              id="input-3"
              v-model="form.message"
              placeholder="Your message here..."
              rows="6"
              class="line"
            ></b-form-textarea>
          </b-form-group>
          <div class="bottom-line"></div>
          <b-button class="btn btn-action" type="submit" variant="primary"
            >Send message</b-button
          >
        </b-form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "TestimonialsClients",
  data() {
    return {
      form: {
        email: "",
        name: "",
        message: "",
      },
      show: true,
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
  },
};
</script>
<style scoped>
.background-testimonial {
  position: absolute;
  width: 100vw;
  top: 4583px;
  z-index: -1;
  display: flex;
  left: 0;
}
.text {
  width: 570px;
  height: 175px;
  margin: auto;
  margin-top: 100px;
  margin-bottom: 70px;
}
.small.text {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 27px;
  text-align: center;
  color: #222A41;
  margin-bottom: 10px;
}
.title {
  font-style: normal;
  font-weight: bold;
  font-size: 60px;
  line-height: 80px;
  text-align: center;
  letter-spacing: -1.85143px;
  color: #222A41;
  margin-bottom: 10px;
}
.description {
  height: 48px;
  width: 332px;
  font-style: normal;
  font-weight: normal;
  font-size: 15px;
  line-height: 24px;
  text-align: center;
  color: #6D7783;
  margin: auto;
}
.clients {
  width: 980px;
  height: 101px;
  margin: auto;
  margin-top: 70px;
  margin-bottom: 51px;
  display: flex;
  justify-content: space-between;
}
.carousel {
  height: 370px;
  width: 895px;
  margin: auto;
}
.carousel-indicators {
  width: 222px;
  height: 6px;
  margin: 60px 310px 0px 410px;
}
.carousel-indicator {
  height: 6px;
  width: 50px;
  background: #DBDBDB;
  border: none;
}
.testimony {
  display: flex;
  flex-direction: row;
  height: 370px;
  justify-content: space-between;
}
.info-card {
  text-align: left;
  height: 135px;
  width: 475px;
}
.img {
  margin-bottom: 30px;
}
.photo-person {
  background: #B4B4B4;
  box-shadow: 40px 40px 80px rgba(0, 0, 0, 0.5);
  border-radius: 18px;
  width: 306px;
  height: 369px;
  transform: matrix(1, 0, 0, 1, 0, 0);
}
.quote {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 27px;
  color: #222A41;
  margin-bottom: 30px;
}
.person {
  font-style: normal;
  font-weight: bold;
  font-size: 21px;
  line-height: 26px;
  color: #000000;
}
.function {
  font-weight: 200;
  margin-bottom: 66px;
}
.contact-form {
  width: 644px;
  height: 556px;
  filter: drop-shadow(0px 2px 8px rgba(0, 0, 0, 0.1));
  background: #FFFFFF;
  box-shadow: 0px 20px 60px rgba(0, 0, 0, 0.2);
  border-radius: 18px;
  margin: auto;
  margin-bottom: 110px;
  margin-top: 190px;
}
.infomessage {
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: 27px;
  text-align: center;
  color: #222A41;
  padding-top: 60px;
  padding-bottom: 60px;
}
.form {
  height: 349px;
  width: 474px;
  margin: auto;
}
.btn-action {
  background: #459EFF;
  box-shadow: 0px 14px 30px rgba(69, 158, 255, 0.2);
  border-radius: 25px;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  color: #FFFFFF;
  height: 50px;
  width: 154px;
  margin-bottom: 60px;
  margin-top: 29px;
}
.line {
  border: none;
}
.bottom-line {
  height: 1px;
  width: 474px;
  background: #AEB7C1;
  margin-bottom: 6px;
}
.carousel-inner {
  border-radius: 18px;
}
.carousel-indicators .active {
  background: #459EFF;
}
</style>
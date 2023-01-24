<template>
  <div class="container">
    <div class="pink-background centered">SCROLL DOWN</div>
    <section class="text-messages-container">
      <div class="preferences">PREFERENCES</div>
      <div class="particular">
        <span>Particular about</span>
        <span>your laundry? Us too.</span>
      </div>
      <div class="text-messages">
        <TextMessage
          msg="Delicate wash?"
          :sent="true"
          :opacity="1"
          data-aos="fade-left"
        />
        <TextMessage
          msg="Done!"
          :sent="false"
          :opacity="1"
          data-aos="fade-right"
        />
        <TextMessage
          msg="Hang dry?"
          :sent="true"
          :opacity="0.5"
          data-aos="fade-left"
        />
        <TextMessage
          msg="Happy to!"
          :sent="false"
          :opacity="0.5"
          data-aos="fade-right"
        />
        <TextMessage
          msg="Special Requests?"
          :sent="true"
          :opacity="0.25"
          data-aos="fade-left"
        />
        <TextMessage
          msg="Welcome!"
          :sent="false"
          :opacity="0.25"
          data-aos="fade-right"
        />
      </div>
      <RoundButton text="REQUEST A PICKUP" />
    </section>
    <div class="pink-background centered">SCROLL UP</div>
  </div>
</template>

<script>
import TextMessage from "./components/TextMessage.vue";
import RoundButton from "./components/RoundButton.vue";
import AOS from "aos";

export default {
  name: "App",
  components: {
    TextMessage,
    RoundButton,
  },
  mounted() {
    AOS.init();
  },
};
</script>

<style>
@font-face {
  font-family: "Pitch Sans";
  src: local("Pitch Sans"),
    url(./assets/PitchSans-Regular.ttf) format("truetype");
}
html,
body {
  margin: 0px;
  font-family: Pitch Sans;
}
.preferences {
  color: #ed6c89;
  font-size: 12px;
  font-weight: 800;
  line-height: 16px;
  letter-spacing: 0.08em;
  text-align: center;
  margin-top: 48px;
  margin-bottom: 12px;
}
.particular {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  font-size: 24px;
  line-height: 24px;
  letter-spacing: -0.08em;
}
.container {
  display: flex;
  flex-direction: column;
}
.pink-background {
  background-color: #ed6c89;
  height: 100vh;
  width: 100%;
}
.centered {
  display: flex;
  justify-content: center;
  align-items: center;
}
.text-messages {
  margin: 36px auto;
  overflow-x: hidden;
  max-width: 800px;
}
.text-messages-container {
  background-color: #f4f4ef;
  align-items: center;
  padding: 24px 0;
}
</style>

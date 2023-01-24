<template>
  <button class="round-button">
    <span class="button-text">{{ text }}</span>
    <span class="circle-icon"
      ><img class="arrow" src="../assets/arrow.png"
    /></span>
  </button>
</template>

<script>
export default {
  name: "RoundButton",
  props: {
    text: {
      type: String,
      required: true,
      default: "",
    },
  },
};
</script>

<style scoped>
.round-button {
  background-color: #ed6c89;
  color: #ffffff;
  border-radius: 100px;
  border: none;
  text-align: center;
  padding: 16px;
  height: 64px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.button-text {
  font-size: 16px;
  line-height: 16px;
  letter-spacing: 0.08em;
  padding: 0 12px;
}
.circle-icon {
  width: 48px;
  height: 48px;
  margin-right: -8px;
  background: rgb(255, 255, 255, 0.32);
  box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.08);
  border-radius: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.arrow {
  width: 40%;
}
</style>

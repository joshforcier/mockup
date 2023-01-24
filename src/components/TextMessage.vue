<template>
  <div
    class="text-message"
    :style="{ justifyContent: justify, opacity: opacity }"
  >
    <div class="text" :style="{ backgroundColor: textColor }">
      {{ msg }}
    </div>
  </div>
</template>

<script>
export default {
  name: "TextMessage",
  props: {
    msg: {
      type: String,
      required: true,
      default: "",
    },
    sent: {
      type: Boolean,
      required: true,
      default: false,
    },
    opacity: {
      type: Number,
      required: true,
      default: 1,
    },
  },
  computed: {
    textColor() {
      return this.sent ? "#9CCFFB" : "#FFFFFF";
    },
    justify() {
      return this.sent ? "right" : "left";
    },
  },
};
</script>

<style scoped>
.text-message {
  display: flex;
}

.text {
  border-radius: 8px;
  height: 48px;
  width: fit-content;
  font-size: 32px;
  font-weight: 550;
  line-height: 44px;
  letter-spacing: -0.08em;
  text-align: right;
  box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.08);
  margin: 12px 24px;
  padding: 0 8px;
}
</style>

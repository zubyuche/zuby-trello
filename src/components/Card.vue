<script>
export default {
  props: ["id"],
  data() {
    return {
      message: "",
      id: 1,
      inputVisible: false,
      textVisible: false,
    };
  },
  methods: {
    selectInput() {
      this.inputVisible = !this.inputVisible;
      this.textVisible = !this.textVisible;
    },
  },
};
</script>

<template>
  <div class="card-container">
    <p class="card-content" @click="selectInput" :class="{ disable: textVisible }">{{ message }}</p>
    <textarea
      class="disable"
      type="text"
      maxlength="275"
      v-model="message"
      @keydown.enter="selectInput"
      :class="{ active: inputVisible }"
    ></textarea>
  </div>
</template>

<style>
.card-container {
  min-height: 20px;
  width: 240px;
  margin-left: 7px;
  margin-right: 10px;
  border-radius: 3px;
  padding: 7px 10px 2px;
  position: relative;
  background-color: whitesmoke;
  display: flex;
  align-items: center;
  box-shadow: 0 2px 2px rgba(2, 2, 2, 0.2);
  cursor: pointer;
  margin-bottom: 8px;
}
.card-content {
  width: 240px;
  height: 100%;
  font-size: 18px;
}
textarea {
  border: none;
  background: inherit;
  cursor: pointer;
  outline: none;
  width: 240px;
  overflow: auto;
  resize: none;
  height: 100%;
  font-family: "Roboto", sans-serif;
  font-size: 14px;
}
.disable {
  display: none;
}
</style>
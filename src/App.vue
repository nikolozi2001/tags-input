<script>
import TagsInput from "./components/TagsInput.vue";

export default {
  data: () => {
    return {
      jsFramework: ["react.js", "vue.js", "angular"],
    };
  },
  mounted() {
    setTimeout(() => {
      this.jsFramework.push("ember.js");
    }, 3000);
  },
};
</script>

<template>
  <h1>Hello World</h1>

  <tags-input />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

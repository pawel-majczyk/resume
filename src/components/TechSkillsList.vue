<template>
  <p class="tech-skills">
    <b v-for="skill in skills" :key="skill">{{ skill }}</b>
  </p>
</template>
<script>
export default {
  props: {
    skills: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

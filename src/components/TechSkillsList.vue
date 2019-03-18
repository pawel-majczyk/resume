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
<style lang="scss" scoped>

.technologies {
  .tech-skills {
    font-size: 1.2em;
    font-weight: 800;
    font-family: 'Trebuchet MS',
    'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    // display: grid;
    // grid-gap: 0.1em;
    // grid-template-columns: 1fr 1fr;
    display: flex;
    flex-wrap: wrap;

    margin: 1em 2em;

    &>b {
      display: inline;
      margin: 0.125em;
      padding: 0.4em;
      color: #366;
      background-color: #eee;
      text-align: center;
    }
  }
}
</style>

<template>
  <section>
    <h2 class="section-head">{{ sectionTitle }}</h2>
    <slot />
  </section>
</template>
<script>
export default {
  props: {
    sectionTitle: {
      type: String,
      default: '',
    },
  },

};
</script>
<style lang="scss" scoped>
.section-head {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  letter-spacing: 1px;
  font-weight: 200;
  margin: 1em 1em 0.5em 0.5em;
  // display: inline-block;
  color: white;
  padding: 0.1em 0.4em;
  background-color: #366;
  position: relative;
  @media only print {
    color: #366;
    background-color: #ccc;
    border-bottom: 0.05em dashed #366;
  }
}
</style>

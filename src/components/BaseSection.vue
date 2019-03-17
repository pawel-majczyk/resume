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

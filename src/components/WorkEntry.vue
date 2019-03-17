<template>
  <li>
    <time>
      <slot name="timespan">
        {{ entry.timespan[0] }} -
        {{ entry.timespan[1] }}
      </slot>
    </time>
    <h3 class="work__company work__company--minor">
      <slot name="company">{{ entry.company }}</slot> -
      <slot name="title">{{ entry.title }}</slot>
    </h3>
    <p class="work__minor-description">
      <slot name="descritpion">
                {{ entry.description }}
      </slot>
    </p>
  </li>
</template>
<script>
export default {
  props: {
    entry: {
      type: Object,
      default: () => ({
        company: 'Company name',
        title: 'job title',
        timespan: 'since-end',
        descritpion: 'description...',
      }),
    },
  },
};
</script>

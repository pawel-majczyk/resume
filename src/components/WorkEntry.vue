<template>
  <li>
    <time>
      <slot name="timespan">
      </slot>
    </time>
    <h3 class="work__company work__company--minor">
      <slot name="company">Convel Sp. j.</slot> -
      <slot name="title">Manufacturing Production Technician</slot>
    </h3>
    <p class="work__minor-description">
      <slot name="descritpion">
                SMT Line Managment;
                quality assurance;
                documentation management
      </slot>
    </p>
  </li>
</template>

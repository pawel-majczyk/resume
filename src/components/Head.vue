<template>
<header class="header">
      <h1 class="header__title">Paweł Majczyk
          <br />
        <span class="header__subtitle">Front-End Developer</span>
      </h1>
      <hr class="divider1" />
      <section class="contact">
        <ul class="contact__list">
          <li>
            <a href="tel:+48605685607"><i class="fas fa-phone-square">
              </i> +48 <b>605&nbsp;685&nbsp;607</b></a>
          </li>
          <li>
            <a href="mailto:pawel.majczyk@gmail.com">
              <i class="fas fa-envelope-square"></i> pawel.majczyk@gmail.com</a>
          </li>
          <li>
            <a href="https://www.linkedin.com/in/pmajczyk">
              <i class="fab fa-linkedin"></i> linkedin.com/in/pmajczyk</a>
          </li>
          <li>
            <a href="https://github.com/pawel-majczyk">
              <i class="fab fa-github-square"></i> github.com/pawel&#8209;majczyk</a>
          </li>
        </ul>
      </section>
    </header>
</template>
<script>
export default {
  data() {
    return {
      test: 'test',
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  &__title {
    padding: 0.25em;
    line-height: 0.80em;
    font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
    font-size: 3em;
    font-weight: 600;
    display: inline-block;
  }
  &__subtitle {
      font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
      line-height: 0.1em;
      font-size: 0.4em;
      text-transform: uppercase;
      font-weight: 100;
      letter-spacing: 0.34em;
      color: #7a7a7a;
  }
  .contact ul {
    display: grid;

    list-style: none;
    margin: 0 auto;
    @media screen AND (min-width: 580px) {
      grid-template-columns: 1fr 1fr;
    }
    @media print {
      grid-template-columns: 1fr 1fr;
    }
    li {
      display: inline-block;
      padding: 0.3em 1em;
      .fas::before,
      .fab::before {
        color: teal;
      }
    }
    a,
    a:visited,
    a:active {
      color: black;
      text-decoration: none;
    }
  }
}
</style>

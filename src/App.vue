<template>
  <div id="app">
    <div class="flex_container">
    <Head />
      <div class="layout_wrapper">
      <section class="work">
        <h2 class="section-head">Work experience</h2>
        <div class="work__current"><time>02.2018 - now </time>
          <h3 class="work__company work__company--current">Bricodes</h3>
          <h3 class="work__job-title">Junior Front-End Developer</h3>
          <div class="work__details">
            Have opportunity to deliver small SPA applications for marketing purposes.<br />
            My main responsibilities were:
            <ul>
              <li>Creating responsive layouts for given design</li>
              <li>Providing CSS animations</li>
              <li>Designing basic components in VueJS framework</li>
            </ul>
            <p>
              Company excels on rapid deployment of games,
              quizes and other entertaiment solutions for
               agencies leading marketing campaigns
              </p>
          </div>
        </div>
        <hr class="divider2" />
        <ul class="work__rest">
          <li><time>02.2017 - now </time>
          <h3 class="work__company work__company--minor">
            Convel Sp. j. - Manufacturing Production Technician</h3>
            <p class="work__minor-description">
              SMT Line Managment;
              quality assurance;
              documentation management</p>
          </li>
          <li><time>08.2014 - 01.2017 </time>
          <h3 class="work__company work__company--minor">
            CM International SA – Production Technician</h3>
            <p class="work__minor-description">
              Electronics assembly;
              quality assurance;
              service works</p>
          </li>
          <li><time>02.2007 - 01.2014 </time>
          <h3 class="work__company work__company--minor">
            WABCO Polska Sp. z o.o. – Production Worker</h3>
            <p class="work__minor-description">
              SMT Operator;
              final assembly and testing</p>
          </li>
          <li><time>05.2006 - 09.2006 </time>
          <h3 class="work__company work__company--minor">
            Triada PC – Office Assistant</h3>
            <p class="work__minor-description">
              advertisement design;
              website administration;
              database management;
              client service</p>
          </li>
        </ul>
      </section>
      <aside class="sidebar">
        <section class="summary">
          <h2 class="section-head">Summary</h2>
          <p>Front-End developer living in <b>Warsaw</b>, Poland</p>
          <p>Specializes in Javascript-based Single&nbsp;Page Applications</p>
          <p>I am looking for long-term business relation.
            Always open to aquire new knowledge, thus constantly attending online courses,
            and available workshops</p>
        </section>
        <section class="technologies">
        <h2 class="section-head">Technologies</h2>
          <p class="tech-skills">
            <b>Javascript</b>
            <b>HTML</b>
            <b>CSS</b>
            <b>Git</b>
            <b>VueJS</b>
            <b>ESlint</b>
            <b>RWD</b>
            <b>Webpack</b>
            <b>Babel</b>
            <b>NPM</b>
            <b>BEM</b>
            <b>SCSS</b>
            <b>Zeplin</b>
            <b>Photoshop</b>
            <b>Inkscape</b>
          </p>
        </section>
        <section class="additional">
        <h2 class="section-head">Additional info</h2>
          <p>
            <ul>
              <li>Good understading of spoken, and written English (B2)</li>
              <li>Proficiency in editing both vector and raster images
                (also 3D model texturing)</li>
              <li>Basic knowledge of Game Design principles</li>
              <li>Eye for aesthetics</li>
              <li>Commitment to craft quality code</li>
            </ul>
          </p>
        </section>
        <section class="personal">
        <h2 class="section-head">Personal interests</h2>
          <p>
            Social Dancing (UrbanKiz, Zouk), sci-fi, detective&nbsp;stories
          </p>
        </section>

      </aside>
      </div>
    </div>
    <div class="flex_container flex_container--footer">
    <footer>
      <p class="legal-notes">"I hereby authorize you to process my personal
         data included in my job application for the
         needs of the recruitment process
         (in accordance to the Personal Data
          Protection Act 29.08.1997 no 133 position 883)."
    </p>
    </footer>
    </div>
  </div>
</template>

<script>
import Head from './components/Head.vue';


export default {
  name: 'app',
  components: { Head },
};
</script>

<style lang="scss">

* {
  margin: 0;
  padding: 0;
}
#app {
  min-height: 100vh;
  @media print {
    width: 100%;
  }
  width: 80%;
  margin: 0 auto;

  display: flex;
  flex-direction: column;

  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-weight: 200;
  font-size: 18px;
  @media print {
    font-size: 12px;
  }
}
.flex_container {
  flex: 1;
  // flex-basis: 100%;
}
.flex-container--footer {
  flex: 0 0 2em;
}

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
.layout_wrapper {
  display: flex;
}
.sidebar {
  font-size: 0.85em;
  flex-basis: 40%;
}
.work {
  flex: 1;
  flex-basis: 60%;
  @media only print {
    p, li {
      font-size: 1.25em;
    }
  }
  .work__current {
    padding: 1em;
    font-size: 1.2em;
  }
  .work__company {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
  .work__company--current {
    font-size: 1.75em;
    color: #366;
  }
  .work__details {
    padding: 0.2em;
    ul {
      margin: 1em 0;
    }
  }

  .work__rest {
    padding: .8em;
    font-size: 0.95em;
    list-style: none;
    li {
      .work__company--minor {
        color: #366;
      }
      padding: 0.5em;
    }
  }
}
.additional, .personal, .summary {
  p {
    padding: 0 3em;
  }
}
.summary {
  p {
    font-size: 1.25em;
    font-weight: 400;
    padding: 0em 0.75em;
    margin-bottom: 1em;
  }

}
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

    b {
      display: inline;
      margin: 0.125em;
      padding: 0.4em;
      color: #366;
      background-color: #eee;
      text-align: center;
    }
  }
}
.legal-notes {
  margin: 1em;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: #666;
}
</style>

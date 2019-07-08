<template>
  <div id="app">
    <div class="flex_container">
    <Head />
    <div class="layout_wrapper">
      <BaseSection class="work" sectionTitle="Work experience" >
        <div class="work__current"><time>02.2018 - now </time>
          <h3 class="work__company work__company--current">
            Bricodes
            <span class="work__part-time">
              part-time
          </span>
          </h3>
          <h3 class="work__job-title">Junior Front-End Developer</h3>
          <div class="work__details">
            Have opportunity to deliver small SPA applications for marketing purposes.<br />
            My main responsibilities are:
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
          <WorkEntry v-for="(entry, index) in data.workExperience.past"
            :key="index"
            :entry="entry"
          />
        </ul>
      </BaseSection>

      <aside class="sidebar">
        <BaseSection class="summary" sectionTitle="Summary" >
          <p>Front-End developer living in <b>Warsaw</b>, Poland</p>
          <p>Specializes in Javascript-based Single&nbsp;Page Applications</p>
          <p>I am looking for a fulltime, long-term business relation.
            Always open to aquire new knowledge, thus constantly attending online courses,
            and available workshops</p>
        </BaseSection>

        <BaseSection class="technologies" sectionTitle="Technologies" >
          <TechSkillsList :skills="data.technologies" />
        </BaseSection>

        <BaseSection class="additional" sectionTitle="Additional info" >
          <p>
            <ul>
              <li v-for="item in data.additionalInfo" :key="item">
                {{ item }}
              </li>
            </ul>
          </p>
        </BaseSection>

        <BaseSection class="personal" sectionTitle="Personal interests" >
          <p>
            Social Dancing (UrbanKiz, Zouk), sci-fi, detective&nbsp;stories
          </p>
        </BaseSection>
      </aside>
      </div> <!-- layout wrapper end -->
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
import BaseSection from './components/BaseSection.vue';
import WorkEntry from './components/WorkEntry.vue';
import TechSkillsList from './components/TechSkillsList.vue';

import cvData from './data.json';

export default {
  name: 'app',
  data() {
    return {
      data: cvData,
    };
  },
  components: {
    Head,
    BaseSection,
    WorkEntry,
    TechSkillsList,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}

#app {
  min-height: 100vh;
  width: 90%;
  @media only screen AND (min-width: 680px) {
    width: 80%;
  }
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
}
.flex-container--footer {
  flex: 0 0 2em;
}
.layout_wrapper {
  display: flex;
  flex-direction: column;
  @media only screen AND (min-width: 800px) {
  flex-direction: row;
  }
  @media print {
    flex-direction: row;
  }
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
  &__current {
    padding: 1em;
    font-size: 1.2em;
  }
  &__company {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
  &__company--current {
    font-size: 1.75em;
    color: #366;
  }
  &__part-time {
    font-weight: 200;
    font-size: 0.5em;
    display: inline-block;
    text-transform: uppercase;
    padding: 0.2em .5em;
    background: #eee;
    color: #666;
    transform: translateY(-0.25em);
    font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  }
  &__details {
    padding: 0.2em;
    ul {
      margin: 1em 0;
    }
  }
  &__rest {
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

.legal-notes {
  margin: 1em;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: #666;
}
</style>

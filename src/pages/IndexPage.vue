<script>
import ProfileComponent from 'src/components/ProfileComponent.vue';
import MenuBar from 'src/components/MenuBar.vue';
import TopBar from 'src/components/TopBar.vue';
import ContactInformations from 'src/components/ContactInformations.vue';
import SeparatorCat from 'src/components/SeparatorCat.vue';
import ProjectContainer from 'src/components/ProjectContainer.vue';

import { defineComponent } from 'vue';
export default defineComponent({
  name: 'IndexPage',
  components: {
    ProfileComponent,
    MenuBar,
    TopBar,
    ContactInformations,
    SeparatorCat,
    ProjectContainer,
  },
  data: () => {
    return {
      projects: [
        {
          name: 'AirtagsAnywhere',
          description:
            'AirtagsAnywhere allows you to use and track your Airtags with a non-Apple device.',
          image: 'https://img.dylanakp.dev/airtags-logo.png',
          link: 'https://github.com/DylanAkp/AirtagsAnywhere',
        },
        {
          name: 'Luna Game Launcher',
          description:
            'Luna Game Launcher is a simple game launcher. Inspired by PlayNite, it allows you to launch your games from a single interface.',
          image: 'https://img.dylanakp.dev/luna-logo.png',
          link: 'https://github.com/DylanAkp/luna-game-launcher',
        },
        {
          name: 'NothingQuickTools',
          description:
            'Provides some useful quick tiles missing on the Nothing Phone (2) by editing settings props.',
          image: 'https://img.dylanakp.dev/nqt-logo.png',
          link: 'https://github.com/DylanAkp/NothingQuickTools',
        },
        {
          name: 'MaterialGPT',
          description:
            'MaterialGPT is an Android application that allows you to use the GPT-3.5/GPT-4 API. It is based on the Google Message design.',
          image: 'https://img.dylanakp.dev/materialgpt-logo.png',
          link: 'https://github.com/DylanAkp/MaterialGPT',
        },
      ],
    };
  },
});
</script>

<template>
  <TopBar />
  <MenuBar />
  <div class="bubble-container align-height">
    <ProfileComponent />
    <ContactInformations />
  </div>
  <SeparatorCat name="Projects" />
  <div class="bubble-container">
    <ProjectContainer
      v-for="(project, index) in projects"
      :key="index"
      :project="project"
    />
  </div>
</template>

<style scoped>
.projects {
  margin-top: 50px;
  margin-left: 5vw;
  margin-right: 5vw;
  display: block;
  justify-content: center;
  flex-wrap: wrap;
}
</style>

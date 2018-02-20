<template>
  <div id="projects">
    <div id="projects_links">
      <div class="tabs">
        <div class="projects_title">
          <span class="sf sf-navigation-o"></span>
          MY PROJECTS
        </div>
        <ul class="tab-links">
          <li v-for="(tabLink, index) in tabLinks"
              :class="{active: activeTab == index}"
              @click.prevent="changeTabLink(index)">
            <a :href="'#tab'+index">
              <span> - </span> {{ tabLink.name }}
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div id="projects_panel">
      <fade-transition group>
        <div v-for="(tabLink, index) in tabLinks"
          class="tab"
          :key="index"
          :class="{active: activeTab == index}"
          :id="'tab' + index"
          :style="{backgroundImage: 'url(' + tabLink.image + ')'}"
          v-show="tabLink.show">
          <div class="tab_hover">
            <h1>{{ tabLink.name }}</h1>
            <div class="tab_description">
              {{ tabLink.description }}
            </div>
          </div>
        </div>
       </fade-transition>
    </div>

    <router-link :to="'/'">
      <div class="close">
          <span id="close" class="sf sf-cross-o spin"></span>
      </div>
    </router-link>
  </div>
</template>

<script>
import projects from '../data/projects';
export default {
  name: 'Projects',
  data() {
    return {
      tabLinks: projects.tabLinks,
      activeTab: -1
    }
  },
  methods: {
    changeTabLink(index) {
      // deselect current active link
      if(this.activeTab == index) {
        // to show the 1st tab
        if(index > 2) {
          this.tabLinks[0].show = true;
        }
        this.activeTab = -1;
        return false;
      }
      this.activeTab = index;
      if(index > 2) {
        this.tabLinks[0].show = false;
      } else if(index == 0) {
        this.tabLinks[0].show = true;
      }
    },
    spin() {
      var x = document.getElementById('close');
      x.classList.add("spin");
    }
  }
}
</script>

<style scoped>
  @import '../css/style.css';
</style>

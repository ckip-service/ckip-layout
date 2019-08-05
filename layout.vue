<template>
  <v-app class="Layout">

    <Nav>
      <v-app-bar-nav-icon slot="nav-icon" @click.stop="drawer = !drawer"/>
      <slot slot="brand" name="nav-brand" />
      <slot name="nav" />
    </Nav>

    <v-navigation-drawer
      app
      clipped
      v-model="drawer"
      class="white"
      :width="sidebarWidth"
    >
      <slot name="sidebar" />
    </v-navigation-drawer>

    <v-content class="milk-light">
      <slot />
    </v-content>

    <Footer :designer="designer">
      <slot name="footer" />
    </Footer>

  </v-app>
</template>

<script>
import './layout.scss';

import Nav from './nav.vue';
import Footer from './footer.vue';

export default {
  name: 'Layout',
  components: {
    Nav,
    Footer,
  },
  props: [
    'designer',
    'sidebarWidth',
  ],
  data() {
    return {
      drawer: null,
    }
  }
};
</script>

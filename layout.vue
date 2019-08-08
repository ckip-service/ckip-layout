<template>
  <v-app class="Layout">

    <Nav
      :right="right"
      :props="navProps"
    >
      <v-app-bar-nav-icon slot="nav-icon" @click.stop="sidebar = !sidebar"/>
      <slot slot="brand" name="nav-brand" />
      <slot name="nav" />
    </Nav>

    <v-navigation-drawer
      app
      clipped
      class="white"
      v-model="sidebar"
      :right="right"
      v-bind="sidebarProps"
    >
      <slot name="sidebar" />
    </v-navigation-drawer>

    <v-content
      class="milk lighten-5"
      v-bind="contentProps"
    >
      <slot />
    </v-content>

    <Footer
      :designer="designer"
      :props="footerProps"
    >
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
    'navProps',
    'footerProps',
    'contentProps',
    'sidebarProps',
    'right',
    'designer',
  ],
  data() {
    return {
      sidebar: null,
    }
  },
};
</script>

<template>
  <v-app class="Layout milk-light">
    <Nav><slot slot="brand" name="nav-brand" /><slot name="nav" /></Nav>
    <v-navigation-drawer app clipped class="grey lighten-5"><slot name="sidebar" /></v-navigation-drawer>
    <v-content><slot /></v-content>
    <Footer :designer="designer"><slot name="footer" /></Footer>
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
  ],
};
</script>

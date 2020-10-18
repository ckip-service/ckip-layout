<template>
  <div class="Layout min-vh-100 d-flex flex-column bg-milk-light" >
    <Nav :fluid="fluid" :toggleable="toggleable">
      <slot slot="brand" name="nav-brand" />
      <slot name="nav" />
      <slot slot="right" name="nav-right" />
    </Nav>

    <div class="flex-grow-1">
      <slot />
    </div>

    <Footer :fluid="fluid" :designer="designer">
      <slot name="footer" />
    </Footer>
  </div>
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
    'fluid',
    'designer',
    'toggleable',
  ],
};
</script>

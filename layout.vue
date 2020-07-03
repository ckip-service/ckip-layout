<template>
  <div class="Layout min-vh-100 d-flex flex-column bg-milk-light" >
    <Nav>
      <slot slot="brand" name="nav-brand" />
      <slot name="nav" />
    </Nav>

    <div class="flex-grow-1 position-relative">
      <div class="position-absolute h-100 w-100">
        <slot />
      </div>
    </div>

    <Footer :designer="designer">
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
    'designer',
  ],
};
</script>

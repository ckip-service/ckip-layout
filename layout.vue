<template>
  <div class="Layout min-vh-100 d-flex flex-column bg-milk-light" >
    <Nav><slot slot="brand" name="nav-brand" /><slot name="nav" /></Nav>
    <slot />
    <Footer :designer="designer"><slot name="footer" /></Footer>
  </div>
</template>

<script>
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

<style lang="scss">
@import "./layout";
</style>

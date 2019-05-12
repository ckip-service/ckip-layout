<template>
  <div class="min-vh-100 d-flex flex-column" >
    <Nav />
    <slot />
    <Footer :designer="designer" />
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

<template>
  <div class="shadow-sm border-bottom bg-white w-100">
    <b-navbar variant="white" :toggleable="toggleable" :class="navClass">

      <slot name="brand" />

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>

        <slot />

        <hr />

        <b-navbar-nav class="ml-auto">

          <slot name="right" />

          <b-nav-item
            href="https://ckip.iis.sinica.edu.tw"
            target="_blank"
          >
            CKIP Lab
          </b-nav-item>

          <b-nav-item
            href="http://www.iis.sinica.edu.tw/index_zh.html"
            target="_blank"
          >
            資訊所
          </b-nav-item>

          <b-nav-item
            href="https://www.sinica.edu.tw/ch"
            target="_blank"
          >
            中央研究院
          </b-nav-item>

        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  props: {
    fluid: {
      type: Boolean,
      default: false,
    },
    toggleable: {
      type: [Boolean, String],
      default: 'lg',
    },
  },
  computed: {
    navClass() {
      return this.fluid ? 'container-fluid' : 'container';
    },
  },
};
</script>

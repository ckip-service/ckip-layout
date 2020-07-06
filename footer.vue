<template>
  <footer class="Footer shadow-sm border-top bg-white w-100 py-2">
    <b-container :fluid="fluid" class="d-flex text-muted">
      <div>
        <!-- eslint-disable-next-line -->
        &copy; <b-link href="//ckip.iis.sinica.edu.tw" target="_blank">CKIP Lab</b-link>
        <template v-if="designer.length !== 0">
          {{ '| Web Design:' }}
          <template v-for="(item, key) in designer">
            <template v-if="key !== 0">{{ ', ' }}</template>
            <b-link :href="item.href" target="_blank" :key="key">{{ item.name }}</b-link>
          </template>{{ '.' }}
        </template>
        <slot />
      </div>

      <div class="ml-auto">
        <a
          class="mx-1"
          href="https://github.com/ckiplab"
          target="_blank"
          title="GitHub"
        >
          <font-awesome-icon :icon="['fab', 'github']" />
        </a>
        <a
          class="mx-1"
          href="https://github.com/ckiplab/issue/issues"
          target="_blank"
          title="Bug Report"
        >
          <font-awesome-icon icon="bug" />
        </a>
      </div>
    </b-container>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    fluid: {
      type: Boolean,
      default: false,
    },
    designer: {
      type: Array,
      default() {
        return [
          {
            name: 'Mu Yang',
            href: 'http://muyang.pro',
          },
        ];
      },
    },
  },
};
</script>

<style scoped lang="scss">
.Footer {
  font-size: smaller;
}
</style>

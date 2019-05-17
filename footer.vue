<template>
  <footer class="bg-white border-top w-100 py-2">
    <b-container>
      <small class="text-muted">
        <!-- eslint-disable-next-line -->
        Copyright &copy; <b-link href="//ckip.iis.sinica.edu.tw" target="_blank">CKIP Lab</b-link>. All rights reserved.
        <template v-if="designer.length !== 0">
          {{ '| Design:' }}
          <template v-for="(item, key) in designer">
            <template v-if="key !== 0">{{ ', ' }}</template>
            <b-link :href="item.href" target="_blank" :key="key">{{ item.name }}</b-link>
          </template>{{ '.' }}
        </template>
        <slot />
      </small>
    </b-container>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    designer: {
      type: Array,
      default() {
        return [
          {
            name: 'Mu Yang',
            href: 'https://muyang.pro',
          },
        ];
      },
    },
  },
};
</script>

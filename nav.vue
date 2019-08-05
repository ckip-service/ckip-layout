<template>
  <v-app-bar app dense clipped-left>

    <slot name="nav-icon"/>

    <v-toolbar-title><slot name="brand" /></v-toolbar-title>

    <slot />

    <v-spacer></v-spacer>

    <v-toolbar-items>

      <v-btn
        text
        href="http://ckip.iis.sinica.edu.tw"
        target="_blank"
      >
        CKIP Lab
      </v-btn>

      <v-btn
        text
        href="http://www.iis.sinica.edu.tw/index_zh.html"
        target="_blank"
      >
        資訊所
      </v-btn>

      <v-btn
        text
        href="https://www.sinica.edu.tw/ch"
        target="_blank"
      >
        中央研究院
      </v-btn>

    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
export default {
  name: 'Nav',
};
</script>

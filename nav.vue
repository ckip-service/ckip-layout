<template>
  <div class="bg-light border-bottom w-100">
    <b-navbar variant="light" toggleable="lg" class="container">

      <slot name="brand" />

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>

        <slot />

        <b-navbar-nav class="ml-auto">

          <b-nav-item
            href="http://ckip.iis.sinica.edu.tw"
            target="_blank"
          >
            CKIP Lab
          </b-nav-item>

          <b-nav-item
            href="http://www.iis.sinica.edu.tw/index_zh.html"
            target="_blank"
          >
            中研院資訊所
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
};
</script>

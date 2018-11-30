<template lang="pug">
  div(:class="[$style.enterpriseReady, 'featureSection']")
    vue-grid
      vue-grid-row
        vue-grid-item.vueGridItem(fill='')
          h2 Enterprise ready
        vue-grid-item.vueGridItem
          vue-panel.vuePanel
            vue-panel-body
              vue-icon-chart-line
              h3 SEO
              p
                | We support SEO (document head tags management) and server-side-rendering for search engines that
                | support
                | indexing of JavaScript content. (eg. Google)
        vue-grid-item.vueGridItem
          vue-panel.vuePanel
            vue-panel-body
              vue-icon-certificate
              h3 Best practices
              p
                | A Common style guide, TypeScript, and the best test setup: Automatically guarantee code quality and
                | non-breaking changes.
        vue-grid-item.vueGridItem
          vue-panel.vuePanel
            vue-panel-body
              vue-icon-flag
              h3 i18n
              p
                | Scalable apps need to support multiple languages, easily add and support multiple languages with
                | vue-i18n.
</template>
  

<script lang="ts">
  import VueGrid            from '../../shared/components/VueGrid/VueGrid.vue';
  import VueGridItem        from '../../shared/components/VueGridItem/VueGridItem.vue';
  import VuePanel           from '../../shared/components/VuePanel/VuePanel.vue';
  import VuePanelBody       from '../../shared/components/VuePanel/VuePanelBody/VuePanelBody.vue';
  import VueGridRow         from '../../shared/components/VueGridRow/VueGridRow.vue';
  import VueIconChartLine   from '../../shared/components/icons/VueIconChartLine/VueIconChartLine.vue';
  import VueIconCertificate from '../../shared/components/icons/VueIconCertificate/VueIconCertificate.vue';
  import VueIconFlag        from '../../shared/components/icons/VueIconFlag/VueIconFlag.vue';

  export default {
    components: {
      VueIconFlag,
      VueIconCertificate,
      VueIconChartLine,
      VueGrid,
      VueGridItem,
      VuePanel,
      VuePanelBody,
      VueGridRow,
    },
  };
</script>

<style lang="scss" module>
  @import "../../shared/styles";

  .enterpriseReady {
    display:    block;
    text-align: center;

    i {
      display:    inline-block;
      height:     $font-size-h1;
      width:      $font-size-h1;
      margin-top: $space-unit;
    }

    @include background-gradient($brand-accent, $brand-light-primary, -135deg);
  }
</style>

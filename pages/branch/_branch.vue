<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
    >
      <v-card>
        <v-card-title class="headline">ゆうちょ銀行店名コンバーター</v-card-title>
        <v-card-text>
          <yucho-result />
          <p>ゆうちょ銀行口座の記号を振込み用の店名に変換します</p>
          <p>変換方法は以下のサイトを参考にしています。</p>
          <converter />
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
  import Converter from '~/components/Converter.vue'
  import YuchoResult from '~/components/YuchoResult.vue'

  export default {
    components: {
      Converter,
      YuchoResult,
    },
    head() {
      return {
        titleTemplate: null,
        title: 'サイト名'
      }
    },
    created() {
      let branch = this.$route.params.branch;
    },
  }
</script>

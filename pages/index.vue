<template>
  <v-row
  >
    <v-col
      cols="12"
    >
      <v-card>
        <v-card-title class="headline">ゆうちょ銀行店名コンバーター</v-card-title>
        <v-card-text>
          <converter />
          <yucho-link />
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
  import Converter from '~/components/Converter.vue'
  import YuchoLink from '~/components/YuchoLink.vue'


  export default {
    components: {
      Converter,
      YuchoLink
    },
    head() {
      return {
        titleTemplate: null,
        title: 'サイト名'
      }
    }
  }
</script>

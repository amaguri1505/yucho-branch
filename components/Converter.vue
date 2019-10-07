<template>
  <div class="converter" id="converter">
    <v-layout>
      <v-flex xs-9>
        <v-text-field v-model="symbolNum" class="converter__input">default</v-text-field>
      </v-flex>
      <v-flex xs-3>
        <v-btn c-on:click="redirectToResult" class="converter__btn">検索</v-btn>
      </v-flex>
    </v-layout>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        errors: [],
        symbolNum: '',
      }
    },
    methods: {
      redirectToResult: function (event) {
        if (/^[0-9]{5}$/.text(symbolNum)){
          this.$route.push({ path: '/symbol/' . symbolNum })
        }
      }
    }
  }
</script>

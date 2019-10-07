<template>
  <div class="result__branch">
    {{ branch }}
  </div>
</template>

<script>
  export default {
    validate ({ params }) {
      return /^[008|018|028]$/.test(params.branch);
    },
    created() {
      let branch = this.$route.params.branch;
    },
  }
</script>

<template>
  <v-ons-navigator v-model:page-stack="pageStack"
    @push="pageStack = [...pageStack, $event]"
    @pop="pageStack = pageStack.slice(0, -1)"
  >
  </v-ons-navigator>
</template>

<script>
  import page1 from './Page1.vue';

  export default {
    data() {
      return {
        pageStack: [page1]
      }
    }
  }
</script>

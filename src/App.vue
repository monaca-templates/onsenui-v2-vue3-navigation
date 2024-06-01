<template>
  <v-ons-navigator v-model:page-stack="pageStack"
    @push="pageStack = [...pageStack, $event]"
    @pop="packStage = pageStack.slice(0, -1)"
  >
  </v-ons-navigator>
</template>

<script>
  import page1 from './Page1.vue';
  import page2 from './Page2.vue';

  export default {
    data() {
      return {
        pageStack: [page1]
      }
    }
  }
</script>

<template>
  <v-ons-page>
    <custom-toolbar :back-label="'Page 1'">Page 2</custom-toolbar>
    <p style="text-align: center">This is the second page
      <v-ons-button @click="pop">Pop Page</v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar.vue';
  import app from './App.vue';

  export default {
    methods: {
      pop() {
        this.$emit('pop');
      } 
    },
    components: { customToolbar },
    key: 'key_page2',
  }
</script>

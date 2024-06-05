<template>
  <v-ons-page>
    <custom-toolbar>Page 1</custom-toolbar>
    <p style="text-align: center">
      This is the first page
      <v-ons-button @click="push">Push Page 2</v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar.vue';
  import page2 from './Page2.vue';
  export default {
     methods: {
       push() {
         this.$emit('push', page2);
       }
     },
     components: { customToolbar },
     key: 'key_page1',
  }
</script>

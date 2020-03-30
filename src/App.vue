<template>
  <v-app >
    <v-content >
      <sidebar/>
        <contents/>
    </v-content>
  </v-app>
</template>

<script>

import sidebar from './components/sidebar.vue';
import contents from './components/contents.vue';
export default {
  name: 'App',

  components: {
    contents,
    sidebar
  },

  data: () => ({
    //
  }),
};
</script>

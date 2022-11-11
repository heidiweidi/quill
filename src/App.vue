<template>
  <v-app>
    <Appbar />
    <Sidebar />
      
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
// Components
import Appbar from '@/components/Appbar.vue'
import Sidebar from '@/components/Sidebar.vue';

export default {
  name: 'App',
  components: {
    Appbar,
    Sidebar
  },
  data: () => ({
    //
  }),
}
</script>

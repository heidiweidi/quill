<template>
  <v-layout>
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="12"
          offset-sm="12"
        >
          <About />

          <UsersTable />
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import About from '@/components/About.vue';

export default defineComponent({
  name: 'Home',

  components: {
    About
  },
});
</script>

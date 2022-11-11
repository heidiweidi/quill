<template>
  <v-layout>
    <UsersAdd />
  </v-layout>
</template>


<script>
import { defineComponent } from 'vue';

// Components
import UsersTable from '@/components/users/UsersTable.vue';
import UsersAdd from '@/components/users/UsersAdd.vue';

export default defineComponent({
  name: 'Users',

  components: {
    UsersAdd
  },
});
</script>
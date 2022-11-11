<template>
  <v-layout>
    <UsersTable />
  </v-layout>
</template>


<script>
import { defineComponent } from 'vue';

// Components
import UsersTable from '@/components/users/UsersTable.vue';

export default defineComponent({
  name: 'Accounts',

  components: {
    UsersTable,
  },
});
</script>
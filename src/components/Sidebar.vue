<template>
  <v-navigation-drawer
    v-model="drawer"
    floating
    permanent
  >
    <v-list density="compact" nav>
      
        <v-list-item prepend-icon="mdi-home-city" value="home" title="home" to="/"></v-list-item>
        <v-list-item prepend-icon="mdi-account-group-outline" value="users" title="users" to="users"></v-list-item>
      
    </v-list>
  </v-navigation-drawer>

</template>

<script>
export default {
  name: 'Sidebar',

  data: () => {
    return {
      drawer: true,
      items: [
        { title: 'Home', icon: 'mdi-home-city', link: '/'},
        { title: 'Users', icon: 'mdi-account-group-outline', link: '/users'},
      ],
      rail: true,
    }
  },

}
</script>
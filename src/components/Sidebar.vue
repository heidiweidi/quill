<template>
  <v-navigation-drawer
    v-model="drawer"
    floating
    permanent
  >
    <v-list-item
      two-line
      prepend-avatar="@/../assets/logo.svg"
      title=""
      nav
    >
    </v-list-item>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item prepend-icon="mdi-home-city" title="Home" value="home" href="/"></v-list-item>
      <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users" href="/users"></v-list-item>
      <v-list-item prepend-icon="mdi-account" title="About" value="about" href="/about"></v-list-item>
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
        { title: 'About', icon: 'mdi-account', link: '/about'},
      ],
      rail: true,
    }
  },

}
</script>
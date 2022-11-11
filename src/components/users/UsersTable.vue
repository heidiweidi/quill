<template>
  <v-table
    fixed-header
    height="300px"
  >
    <thead>
      <tr>
        <th class="text-left">
          First Name
        </th>
        <th class="text-left">
          Last Name
        </th>
        <th class="text-left">
          Email
        </th>
        <th class="text-left">
          Username
        </th>
        <th class="text-center">
          Actions
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in users"
        :key="item.firstname"
      >
        <td>{{ item.firstname }}</td>
        <td>{{ item.lastname }}</td>
        <td>{{ item.email }}</td>
        <td>{{ item.username }}</td>
        <td class="dark">
          <div class="d-flex justify-space-around">
            <v-btn variant="flat">Delete</v-btn>
            <v-btn variant="flat">Edit</v-btn>
          </div>
        </td>
      </tr>
    </tbody>
  </v-table>
</template>

<script>
export default {
  name: "UsersTable",
  data: () => ({
    users: [
      {
        firstname: 'Jorge',
        lastname: 'Bush',
        email: 'jorgebush@gmail.com',
        username: 'jbush',
      },
      {
        firstname: 'John',
        lastname: 'Doe',
        email: 'johndoe@gmail.com',
        username: 'johndoe',
      },
      {
        firstname: 'Halle',
        lastname: 'Ka',
        email: 'halleka@yahoo.com',
        username: 'halle_ka',
      },
      {
        firstname: 'Pedro',
        lastname: 'Penduko',
        email: 'ppenduko@gmail.com',
        username: 'ppenduko123',
      },
      {
        firstname: 'Maja',
        lastname: 'Blanca',
        email: 'majablanca@gmail.com',
        username: 'majablanca_213',
      },
    ],
  }),
}
</script>
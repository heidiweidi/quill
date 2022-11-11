<template>
    <v-form
      ref="form"
      v-model="valid"
      lazy-validation
    >
    
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="12"
        >
          <h2>Add User</h2>
        </v-col>
      </v-row>

      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="firstname"
            :counter="10"
            :rules="nameRules"
            label="First Name"
            placeholder="John"
            required
          ></v-text-field>

        </v-col>

        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="lastname"
            :counter="10"
            :rules="nameRules"
            label="Last Name"
            placeholder="Doe"
            required
          ></v-text-field>

        </v-col>

        <v-col
          cols="12"
          md="12"
        >
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            placeholder="email@email.com"
            required
          ></v-text-field>
      
          <v-text-field
            v-model="username"
            :counter="10"
            :rules="nameRules"
            label="Username"
            placeholder="Username"
            required
          ></v-text-field>

          <v-text-field
            v-model="password"
            :counter="10"
            :rules="nameRules"
            label="Password"
            placeholder="password"
            type="password"
            hint="Enter your password to access this website"
            required
          ></v-text-field>

          <v-text-field
            v-model="password2"
            :counter="10"
            :rules="nameRules"
            label="Re-type Password"
            placeholder="re-type password"
            type="password"
            hint="Enter your password to access this website"
            required
          ></v-text-field>

          <v-btn
            color="danger"
            class="mr-4"  
            @click="reset"
          >
            Clear
          </v-btn>

          <v-btn
            color="success"
            class="mr-4"
            @click="validate"
          >
            Add Record
          </v-btn>
        </v-col>
      </v-row>
    </v-container>

    </v-form>
</template>

<script>
  export default {
    data: () => ({
      valid: true,
      firstname: '',
      nameRules: [
        v => !!v || 'First Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      lastname: '',
      nameRules: [
        v => !!v || 'Last Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      username: '',
      nameRules: [
        v => !!v || 'Username is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      password: '',
      nameRules: [
        v => !!v || 'Password did not match',
        v => (v && v.length <= 10) || 'Please re-type password',
      ],
    }),
    
    dialog: false,
    
    methods: {
      async validate () {
        const { valid } = await this.$refs.form.validate()

        if (valid) alert('Form is valid')
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
    },
  }
</script>
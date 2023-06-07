<template>
  <v-sheet class="bg-deep-purple pa-12" rounded>
    <v-card class="mx-auto px-6 py-8" max-width="344">
      <v-form
        v-model="form"
        @submit.prevent="onSubmit"
        ref="myForm"
      >
        <v-text-field
          v-model="name"
          :readonly="loading"
          :rules="[required]"
          class="mb-2"
          clearable
          label="full name"
        ></v-text-field>
        <v-text-field
          v-model="email"
          :readonly="loading"
          :rules="[required]"
          class="mb-2"
          clearable
          label="Email"
        ></v-text-field>

        <v-text-field
          v-model="password"
          :readonly="loading"
          :rules="passwordRules"
          clearable
          label="Password"
          placeholder="Enter your password"
        :error-messages="passwordErrors"
        ></v-text-field>
         <v-text-field
          v-model="password1"
          :readonly="loading"
          :rules="passwordRules"
          clearable
          label="Compare Password"
          placeholder="Enter your password"
          
          :error-messages="passwordErrors"
        ></v-text-field>
        <br>

        <v-btn
          :disabled="!form"
          :loading="loading"
          block
          color="success"
          size="large"
          type="submit"
          variant="elevated"
           @click="resetForm"
        >
          Register
        </v-btn>
      </v-form>
    </v-card>
  </v-sheet>
</template>
<script>
  export default {
    data: () => ({
      form: false,
      name:null,
      email: null,
      password: null,
      password1: null,
      passwordRules: [
      v => !!v || 'La contraseña es requerida',
      v => (v && v.length >= 8) || 'La contraseña debe tener al menos 8 caracteres',
      v => /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]/.test(v) || 'La contraseña debe contener al menos una letra mayúscula, una letra minúscula, un número y un carácter especial'
      ],
      loading: false,
    }),

    methods: {
      onSubmit () {
        if (!this.form) return

        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
      required (v) {
        return !!v || 'Field is required'
      },
      resetForm() {
      this.$refs.myForm.reset();
    }
    },
 
  }
</script>
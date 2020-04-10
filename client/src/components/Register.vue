<template>
 <div>
   <h1>Register</h1>

   <input
     type="text"
     name="email"
     v-model="email"
     placeholder="email"
   >
   <br>
   <input
     type="text"
     name="password"
     v-model="password"
     placeholder="password"
   >
   <br>
   <button @click="register">Register</button>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'
export default {
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    async register () {
      // eslint-disable-next-line no-unused-vars
      const response = await AuthenticationService.register({
        email: this.email,
        password: this.password
      })
    }
  }
}
</script>

<style scoped>

</style>

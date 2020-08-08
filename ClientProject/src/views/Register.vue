<template>
  <div class="register">
      <RegisterForm msg="Registrarse"/>
  </div>
</template>

<script>
import RegisterForm from '@/components/RegisterForm.vue'

export default {
  name: 'Register',
  components: {
    RegisterForm
  }
}
</script>

<style scoped>
</style>
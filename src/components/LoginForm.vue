<template>
  <div class="login-container d-flex justify-content-center align-items-center vh-100 bg-dark text-white">
    <div class="card p-4 shadow-lg" style="width: 350px;">
      <h3 class="text-center mb-4">Login</h3>

      <form @submit.prevent="handleLogin">
        <div class="mb-3">
          <label for="email" class="form-label">Email</label>
          <input
            v-model="email"
            type="email"
            class="form-control"
            id="email"
            placeholder="Enter email"
            required
          />
        </div>

        <div class="mb-3">
          <label for="password" class="form-label">Password</label>
          <input
            v-model="password"
            type="password"
            class="form-control"
            id="password"
            placeholder="Enter password"
            required
          />
        </div>

        <button type="submit" class="btn btn-primary w-100 mt-3">Login</button>

        <p class="text-center mt-3 mb-0">
          Don't have an account? <a href="#" class="text-decoration-none">Sign up</a>
        </p>
      </form>
    </div>
  </div>
</template>

<script setup>
	import { ref } from 'vue'

	const email = ref('')
	const password = ref('')

	const handleLogin = () => {
	  console.log('Email:', email.value)
	  console.log('Password:', password.value)
	  alert('Login submitted! (Replace with real auth logic)')
	}
</script>

<style scoped>

.login-container {
  background: url('https://images.unsplash.com/photo-1557683316-973673baf926?q=80&w=1200') center/cover no-repeat;
  background-size: cover;
}

.card {
  background-color: rgba(0, 0, 0, 0.85);
  color: #fff;
}

a {
  color: #1f6feb;
}

</style>

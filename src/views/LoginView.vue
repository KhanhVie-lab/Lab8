<template>
  <br /><br />
  <div class="container mt-12">
    <div class="login-card p-4 rounded shadow-lg">
      <h2 class="text-center mb-4">Login</h2>
      <div class="mb-3">
        <label for="email" class="form-label">Email</label>
        <input
          type="email"
          class="form-control"
          id="email"
          v-model="email"
          placeholder="Enter your email"
          required
        />
      </div>
      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input
          type="password"
          class="form-control"
          id="password"
          v-model="password"
          placeholder="Enter your password"
          required
        />
      </div>
      <button @click="login" class="btn btn-success w-100">Login</button>
      <div class="text-center mt-3">
        <router-link to="/register" class="text-decoration-none"
          >Don't have an account? Register</router-link
        >
      </div>
    </div>
  </div>
  <br /><br /><br /><br /><br />
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
    }
  },
  methods: {
    login() {
      // Giả lập quá trình đăng nhập và lưu trạng thái xác thực
      if (this.email === 'khanhvie0911@gmail.com' && this.password === '123456') {
        localStorage.setItem('isAuthenticated', true) // Lưu trạng thái đăng nhập vào localStorage
        alert('Login successful!')
        this.$router.push({ name: 'Dashboard' }) // Chuyển hướng đến Dashboard
      } else {
        alert('Invalid email or password!')
      }
    },
  },
}
</script>

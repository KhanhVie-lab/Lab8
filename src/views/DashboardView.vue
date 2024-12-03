<template>
  <div class="container mt-5">
    <h1 class="display-5">Welcome to Dashboard</h1>
    <p class="mt-3">This is your private Dashboard.</p>

    <!-- Nút Logout -->
    <button @click="logout" class="btn btn-danger">Logout</button>
  </div>
</template>

<script>
export default {
  methods: {
    logout() {
      // Xóa trạng thái xác thực trong localStorage
      localStorage.removeItem('isAuthenticated')

      // Chuyển hướng người dùng về trang Login
      this.$router.push({ name: 'Login' })
    },
  },
}
</script>

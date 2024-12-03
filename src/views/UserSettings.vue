<template>
  <div class="container mt-5">
    <h1 class="display-5">User Settings</h1>
    <form class="mt-4">
      <div class="form-group">
        <label for="emailNotifications">Email Notifications</label>
        <input type="checkbox" id="emailNotifications" v-model="settings.emailNotifications" />
        <span class="ml-2">Enable email notifications</span>
      </div>

      <div class="form-group mt-3">
        <label for="darkMode">Dark Mode</label>
        <input type="checkbox" id="darkMode" v-model="settings.darkMode" />
        <span class="ml-2">Enable dark mode</span>
      </div>

      <div class="form-group mt-4">
        <button @click.prevent="saveSettings" class="btn btn-success">Save Settings</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Cài đặt người dùng (sử dụng v-model để liên kết với các trường)
      settings: {
        emailNotifications: false,
        darkMode: false,
      },
    }
  },
  methods: {
    saveSettings() {
      // Logic để lưu các cài đặt của người dùng (có thể lưu vào localStorage, API, v.v.)
      console.log('Settings saved:', this.settings)
      alert('Settings have been saved!')
    },
  },
}
</script>

<style scoped>
/* Thêm một số kiểu CSS cho giao diện */
.container {
  max-width: 600px;
}
</style>

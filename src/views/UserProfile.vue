<template>
  <div class="container mt-5">
    <h1 class="mb-4">User Profile</h1>
    <div class="btn-group" role="group">
      <router-link to="/profile/info" class="btn btn-outline-primary">Info</router-link>
      <router-link to="/profile/settings" class="btn btn-outline-secondary">Settings</router-link>
    </div>
    <div class="mt-4">
      <router-view />
    </div>
  </div>
</template>

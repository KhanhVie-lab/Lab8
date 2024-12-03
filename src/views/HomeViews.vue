<template>
  <div class="container text-center mt-5">
    <h1 class="display-4">Welcome to <span class="text-primary">MyBlog</span></h1>
    <p class="lead">A simple blog built with Vue.js</p>
    <router-link to="/blog" class="btn btn-primary">View Blogs</router-link> |
    <router-link to="/">Home</router-link> | <router-link to="/login">Login</router-link> |
    <router-link to="/dashboard">Dashboard</router-link> |
    <router-link to="/profile">Profile</router-link>
  </div>
</template>

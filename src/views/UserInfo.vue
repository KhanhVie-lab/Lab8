<template>
  <div class="container my-5">
    <br />
    <h2>User Profile</h2>
    <br />
    <form>
      <div class="text-center">
        <img :src="imageUrl" width="100" class="rounded-circle" />
      </div>
      <div class="mb-3">
        <label for="name" class="form-label">Name</label>
        <input type="text" class="form-control" id="name" value="Trần Văn Khánh Vi" />
      </div>
      <div class="mb-3">
        <label for="email" class="form-label">Email</label>
        <input type="email" class="form-control" id="email" value="khanhvie0911@gmail.com" />
      </div>
      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" class="form-control" id="password" value="09112005" />
      </div>

      <!-- Avatar Upload -->
      <div class="mb-3">
        <label for="avatar" class="form-label">Avatar</label>
        <input type="file" class="form-control" id="avatar" accept="image/*" />
        <img
          alt="Avatar Preview"
          class="mt-2"
          style="width: 100px; height: 100px; object-fit: cover; border-radius: 50%"
        />
      </div>

      <!-- Bio -->
      <div class="mb-3">
        <label for="bio" class="form-label">Bio</label>
        <textarea
          class="form-control"
          id="bio"
          rows="3"
          value="Thỏ bảy màu làm giàu cho bạn"
        ></textarea>
      </div>

      <button type="button" class="btn btn-primary">Update Profile</button>
    </form>
  </div>
  <br />
  <br />
</template>

<script>
export default {
  data() {
    return {
      imageUrl: 'https://www.pngkey.com/png/detail/114-1149847_avatar-unknown-dp.png',
    }
  },
}
</script>

<style scoped>
.container {
  max-width: 1600px;
  width: 800px;
}

img {
  max-width: 100%;
  height: auto;
}
</style>

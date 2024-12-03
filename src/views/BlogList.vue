<template>
  <div class="container mt-5">
    <h1 class="mb-4">Blog List</h1>
    <ul class="list-group">
      <!-- Lặp qua từng blog để hiển thị thông tin -->
      <li v-for="blog in blogs" :key="blog.id" class="list-group-item">
        <!-- Hiển thị hình ảnh blog -->
        <div class="post-img mb-2">
          <img :src="blog.imageUrl" alt="Blog Image" class="img-fluid rounded" />
        </div>
        <!-- Hiển thị tiêu đề blog -->
        <router-link
          :to="{ name: 'BlogPost', params: { id: blog.id, blogData: blog } }"
          class="fw-bold"
        >
          {{ blog.title }}
        </router-link>
        <!-- Nút hành động -->
        <div class="mt-2">
          <button class="btn btn-outline-primary me-2">Like</button>
          <button class="btn btn-outline-success">Share</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      blogs: [
        {
          id: 1,
          title: 'Chị đẹp đạp gió rẽ sóng | Tập 1',
          imageUrl:
            'https://cloudvodhn.tek4tv.vn/attach/crawler/2024/08/31/28afe0d3-c2bc-4cd6-ad53-dc31a0c0ea9a-788.webp',
        },
        {
          id: 2,
          title: 'Thám tử lừng danh Conan | Tập 212: Vụ án giết người trong phòng kín',
          imageUrl: 'https://trungtamnhatngu.edu.vn/uploads/blog/2014_12/connan-nhatngusofl_1.jpg', // Thay bằng URL thực tế
        },
      ],
    }
  },
  methods: {
    viewBlog(id) {
      this.$router.push({ name: 'BlogPost', params: { id } })
    },
  },
}
</script>

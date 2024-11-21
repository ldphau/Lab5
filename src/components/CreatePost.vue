<template>
    <div class="container py-4">
      <h2 class="text-dark mb-4">Tạo bài viết mới</h2>
      <div class="bg-light p-4 rounded shadow-sm">
        <div class="mb-3">
          <label for="title" class="form-label">Tiêu đề bài viết</label>
          <input 
            id="title" 
            v-model="title" 
            type="text" 
            class="form-control" 
            placeholder="Nhập tiêu đề bài viết"
          >
        </div>
        <div class="mb-3">
          <label for="author" class="form-label">Tác giả</label>
          <input 
            id="author" 
            v-model="author" 
            type="text" 
            class="form-control" 
            placeholder="Nhập tên tác giả"
          >
        </div>
        <div class="mb-3">
          <label for="content" class="form-label">Nội dung</label>
          <textarea 
            id="content" 
            v-model="content" 
            class="form-control" 
            rows="5" 
            placeholder="Nhập nội dung bài viết"
          ></textarea>
        </div>
        <button 
          class="btn btn-primary w-100" 
          @click="submitPost"
        >
          Đăng bài
        </button>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const emit = defineEmits(['add-post']);
  
  const title = ref('');
  const content = ref('');
  const author = ref('');
  
  function submitPost() {
    if (title.value && content.value && author.value) {
      const newPost = {
        title: title.value,
        content: content.value,
        author: author.value,
      };
  
      emit('add-post', newPost);
  
      // Reset các trường sau khi đăng bài
      title.value = '';
      content.value = '';
      author.value = '';
    }
  }
  </script>
  
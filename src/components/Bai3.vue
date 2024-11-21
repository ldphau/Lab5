<template>
    <div class="container py-4">
      <div class="row">
        <!-- Form -->
        <div class="col-lg-6 col-md-8 mx-auto">
          <h1 class="text-center mb-4">Thông tin cá nhân</h1>
          <form class="bg-light p-4 rounded shadow-sm">
            <div class="mb-3">
              <label class="form-label">Họ và tên</label>
              <input 
                v-model="userInfo.name" 
                type="text" 
                class="form-control" 
                placeholder="Nhập họ và tên"
              >
            </div>
            <div class="mb-3">
              <label class="form-label">Tuổi</label>
              <input 
                v-model="userInfo.age" 
                type="number" 
                class="form-control" 
                placeholder="Nhập tuổi"
              >
            </div>
            <div class="mb-3">
              <label class="form-label">Email</label>
              <input 
                v-model="userInfo.email" 
                type="email" 
                class="form-control" 
                placeholder="Nhập email"
              >
            </div>
          </form>
        </div>
      </div>
  
      <!-- Display Information -->
      <div class="row mt-4">
        <div class="col-lg-6 col-md-8 mx-auto">
          <div class="info-display p-4 bg-dark text-white rounded shadow-sm">
            <h2 class="text-center">Thông tin đã nhập</h2>
            <p><strong>Họ và tên:</strong> {{ userInfo.name }}</p>
            <p><strong>Tuổi:</strong> {{ userInfo.age }}</p>
            <p><strong>Email:</strong> {{ userInfo.email }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { reactive } from 'vue';
  
  const userInfo = reactive({
    name: '',
    age: null,
    email: ''
  });
  </script>
  
<template>
    <div class="p-3">
        <h3>Bài 2</h3>
        <input v-model="userInput" placeholder="Nhập dữ liệu">
        <p>Giá trị bạn nhập {{ userInput }}</p>
    </div>
</template>

<script setup>
import {ref} from 'vue';
const userInput = ref('')
</script>
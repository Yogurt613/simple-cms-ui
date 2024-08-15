<script setup>
import { ref } from 'vue';

// 綁定表單引用
const form = ref();

// 驗證欄位
const validateField = (e) => {
  const { target } = e;
  target.classList.toggle('is-valid', target.checkValidity());
  target.classList.toggle('is-invalid', !target.checkValidity());
};

// 驗證表單
const validateForm = () => {
  form.value.classList.add('was-validated');
  return form.value.checkValidity();
};

// 暴露屬性
defineExpose({
  validateForm,
});
</script>

<template>
  <form
    ref="form"
    class="border p-3"
  >
    <div class="mb-3">
      <label
        for="name"
        class="form-label"
      >
        Name
      </label>
      <input
        id="name"
        type="text"
        class="form-control"
        required
        @input="validateField"
      >
      <div class="invalid-feedback">
        Please provide a valid name.
      </div>
    </div>
  </form>
</template>

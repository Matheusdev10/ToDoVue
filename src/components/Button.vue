<script setup>
defineEmits(['update:modelValue']);
const props = defineProps({
  title: String,
  type: String,
});
</script>

<template>
  <button
    class="btn btn-primary btn-sm"
    :type="type"
    @button="$emit('update:modelValue')"
  >
    Adicionar
  </button>
</template>

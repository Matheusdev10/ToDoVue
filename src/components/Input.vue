<script setup>
defineEmits(['update:modelValue']);
const props = defineProps({
  type: String,
  placeholder: String,
  modelValue: String,
});
</script>

<template>
  <container>
    <input
      :placeholder="placeholder"
      :value="modelValue"
      :type="type"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </container>
</template>

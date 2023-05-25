<template>
  <div class="mt-2">
    <label class="p-1 px-2 rounded-sm text-white" :class="{ 'bg-slate-600': !modelValue, 'bg-green-600': modelValue }">
      <input type="checkbox" :value="modelValue" @input="() => $emit('update:modelValue')" class="hidden" />
      {{ modelValue ? "Completed" : "Mark as completed" }}
    </label>
  </div>
</template>

<script lang="ts" setup>
defineEmits(["update:modelValue"]);
defineProps({
  modelValue: {
    type: Boolean,
    default: false,
  },
});
</script>

<style scoped>
::selection {
  display: none;
}
</style>

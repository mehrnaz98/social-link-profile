<template>
  <a
    class="flex justify-center items-center bg-[#333333] sm:w-[250px] h-[35px] w-[235px] text-xs font-semibold text-[#D9D9D9] border-none rounded-md hover:bg-[#C4F82A] hover:text-[#1F1F1F]"
    :href="url"
    target="_blank"
    rel="noopener noreferrer"
  >
    <slot></slot>
  </a>
</template>

<script setup>
const props = defineProps({
  url: { type: String, required: true },
});
</script>

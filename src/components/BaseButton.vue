<template>
  <a
    class="flex justify-center items-center bg-[#333333] sm:w-[19.4rem] w-[18.1rem] py-3 text-[0.875rem] font-semibold text-[#D9D9D9] border-none rounded-md hover:bg-[#C4F82A] transition-color duration-200 hover:text-[#1F1F1F] focus:outline-none focus:ring focus:ring-[#BBD37B]"
    :href="url"
    target="_blank"
    rel="noopener noreferrer"
    title="Opens in a new tab"
  >
    <slot></slot>
  </a>
</template>

<script setup>
const props = defineProps({
  url: { type: String, required: true },
});
</script>

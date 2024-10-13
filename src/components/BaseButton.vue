<template>
  <a
    class="flex justify-center items-center bg-[#333333] sm:w-[310px] w-[290px] py-3 text-[14px] font-semibold text-[#D9D9D9] border-none rounded-md hover:bg-[#C4F82A] transition-color duration-200 hover:text-[#1F1F1F] focus:outline-none focus:ring focus:ring-[#BBD37B]"
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

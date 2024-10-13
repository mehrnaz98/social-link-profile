<template>
  <div class="flex justify-center items-center h-screen bg-[#141414]">
    <BaseCard />
    <div class="absolute bottom-3 text-[#D9D9D9] text-xs">
      Challenge by
      <a
        href="https://www.frontendmentor.io?ref=challenge"
        target="_blank"
        class="text-[#BBD37B] hover:font-bold transition-fonts duration-200"
        >Frontend Mentor</a
      >. Coded by
      <a
        href="https://github.com/mehrnaz98/"
        class="text-[#BBD37B] hover:font-bold transition-fonts duration-200"
        >Mehrnaz Eftekhari</a
      >.
    </div>
  </div>
</template>

<script setup>
import BaseCard from "./components/BaseCard.vue";
</script>

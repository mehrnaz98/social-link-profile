<template>
  <section
    class="bg-[#1F1F1F] font-inter border-none rounded-lg sm:w-[310px] h-[490px] w-[280px] flex flex-col justify-center items-center text-center"
  >
    <ProfileInfo />
    <BaseButton />
  </section>
</template>

<script setup>
import BaseButton from "./BaseButton.vue";
import ProfileInfo from "./ProfileInfo.vue";
</script>

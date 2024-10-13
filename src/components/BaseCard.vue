<template>
  <section
    class="bg-[#1F1F1F] font-inter border-none rounded-lg sm:w-[310px] h-[auto] w-[280px] sm:py-7 py-5 flex flex-col justify-center items-center text-center"
  >
    <div class="flex flex-col justify-center items-center">
      <profile-info username="mehrnaz98"></profile-info>
    </div>

    <div
      class="flex flex-col space-y-3 pt-5 justify-center items-center hover:cursor-pointer"
    >
      <base-button
        v-for="(button, index) in buttons"
        :key="index"
        :url="button.url"
        >{{ button.name }}</base-button
      >
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import BaseButton from "./BaseButton.vue";
import ProfileInfo from "./ProfileInfo.vue";

const buttons = ref([
  { name: "GitHub", url: "https://github.com/mehrnaz98" },
  {
    name: "Frontend Mentor",
    url: "https://www.frontendmentor.io/profile/mehrnaz98",
  },
  {
    name: "LinkedIn",
    url: "https://www.linkedin.com/in/mehrnaz-eftekhari-4a401122b",
  },
  { name: "Twitter", url: "https://twitter.com" },
  { name: "Instagram", url: "https://www.instagram.com" },
]);
</script>

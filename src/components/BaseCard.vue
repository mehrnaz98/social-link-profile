<template>
  <main
    class="bg-[#1F1F1F] font-inter border-none rounded-lg sm:min-w-[24.4rem] w-[21.9rem] sm:py-9 py-7 flex flex-col items-center text-center"
  >
    <profile-info username="mehrnaz98"></profile-info>

    <ul class="flex flex-col space-y-4 pt-5">
      <li v-for="(button, index) in buttons" :key="index">
        <base-button :url="button.url">{{ button.name }}</base-button>
      </li>
    </ul>
  </main>
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

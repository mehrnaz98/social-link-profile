<template>
  <section
    class="flex flex-col justify-center items-center min-h-screen bg-[#141414]"
  >
    <main
      class="bg-[#1F1F1F] font-inter border-none rounded-lg sm:w-[390px] w-[350px] sm:py-9 py-7 flex flex-col items-center text-center"
    >
      <profile-info username="mehrnaz98"></profile-info>

      <ul class="flex flex-col space-y-4 pt-5">
        <li v-for="(button, index) in buttons" :key="index">
          <base-button :url="button.url">{{ button.name }}</base-button>
        </li>
      </ul>
    </main>
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

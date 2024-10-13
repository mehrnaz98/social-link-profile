<template>
  <section>
    <div v-if="user">
      <img
        :src="user.avatar_url"
        alt="user profile photo"
        class="w-[88px] h-auto border-none rounded-full m-auto -mb-3"
      />
      <h2 class="font-semibold text-[#D9D9D9] text-2xl pt-7">
        {{ user.name }}
      </h2>
      <p class="text-[#BBD37B] text-[14px] font-semibold pt-1">
        {{ user.location }}
      </p>

      <p class="text-[#B7B7B7] text-[14px] pt-5 px-4">"{{ user.bio }}"</p>
    </div>

    <div v-else>
      <img
        src="../assets/images/image.jpg"
        alt="user profile photo"
        class="w-[88px] h-auto border-none rounded-full m-auto -mb-3"
      />
      <h2 class="font-semibold text-[#D9D9D9] text-2xl pt-7">
        Mehrnaz Eftekhari
      </h2>
      <p class="text-[#BBD37B] text-[14px] font-semibold pt-1">
        Rasht, Guilan, Iran
      </p>

      <p class="text-[#B7B7B7] text-[14px] pt-5 px-4">
        "Mechanical Engineer and Designer; Translator and Content Creator;
        Aspiring Frontend Developer."
      </p>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps({
  username: { type: String, required: true },
});

const user = ref(null);

fetch(`https://api.github.com/users/${props.username}`)
  .then(async (res) => {
    if (res.ok) {
      const data = await res.json();
      user.value = data;
    } else {
      user.value = null;
    }
  })
  .catch(() => {
    user.value = null;
  });
</script>

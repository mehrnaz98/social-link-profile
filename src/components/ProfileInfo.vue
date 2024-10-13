<template>
  <section class="flex flex-col justify-center items-center">
    <div v-if="user">
      <img
        :src="user.avatar_url"
        alt="user profile photo"
        class="w-[75px] h-auto border-none rounded-full"
      />
      <h2 class="font-semibold text-[#D3D3D3] text-xl pt-7">{{ user.name }}</h2>
      <p class="text-[#BBD37B] text-xs font-semibold pt-1">
        {{ user.location }}
      </p>

      <p class="text-[#B7B7B7] text-xs pt-5">"{{ user.bio }}"</p>
    </div>

    <div v-else>
      <img
        src="../assets/images/avatar-jessica.jpeg"
        alt="user profile photo"
        class="w-[75px] h-auto border-none rounded-full m-auto"
      />
      <h2 class="font-semibold text-[#D3D3D3] text-xl pt-7">Jessica Randall</h2>
      <p class="text-[#BBD37B] text-xs font-semibold pt-1">
        London, United Kingdom
      </p>

      <p class="text-[#B7B7B7] text-xs pt-5">
        "Front-end developer and avid reader."
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

fetch(`https://api.github.com/users/${props.username}`).then(async (res) => {
  const data = await res.json();
  user.value = data;
});
</script>

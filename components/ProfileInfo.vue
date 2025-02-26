<template>
  <figure class="p-6">
    <img class="w-32 h-32 rounded-full mx-auto" src="../assets/images/profile-pic.jpg" alt="profile picture" width="400"
      height="400" />
    <div class="pt-6 text-center space-y-4">
      <figcaption class="font-medium">
        <div class="text-yellow-500 text-xl py-2">{{ title }}</div>
        <div class="text-cyan-900 font-light">{{ subtitle }}</div>
      </figcaption>
      <blockquote>
        <p class="text-lg font-medium py-2">{{ headline }}</p>
      </blockquote>
      <hashtag>
        #Made with 💗   
      </hashtag>
    </div>
  </figure>
</template>
<script setup>
const { title, subtitle, headline } = defineProps(['title', 'subtitle', 'headline'])
</script>
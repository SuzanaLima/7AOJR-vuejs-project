<template>
  <figure class="p-6">
    <img 
      class="w-32 h-32 rounded-full mx-auto transition ease-in-out duration-150 image-profile
      border-slate-400 border-1
      hover:scale-110 hover:border-indigo-400 hover:border-2" 
      src="../assets/images/profile-pic.jpg" 
      alt="profile picture" 
      width="400"
      height="400" />
    <div class="pt-6 text-center space-y-4">
      <div class="font-medium">
        <div class="text-yellow-500 text-xl py-2">{{ title }}</div>
        <div class="text-cyan-200 font-light">{{ subtitle }}</div>
      </div>
      <blockquote>
        <p class="text-lg text-white font-medium py-2">{{ headline }}</p>
      </blockquote>
      <div class="text-white py-2">
        #Made with 💗 By Suzana Lima
      </div>
      <div id="welcome" class="text-white py-t-2">
        Sejam bem-vindos!
      </div>
    </div>
  </figure>
</template>
<script setup>
const { title, subtitle, headline } = defineProps(['title', 'subtitle', 'headline'])
import { onMounted } from 'vue';

onMounted(() => {
  const welcomeDiv = document.querySelector('#welcome');
  if (welcomeDiv) {
    const second = 1000;
    setTimeout(() => {
      welcomeDiv.parentNode.removeChild(welcomeDiv);
    }, 5 * second); 
  }
});

</script>
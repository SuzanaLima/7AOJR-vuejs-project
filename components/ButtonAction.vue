<template>
    <div class="pt-6 text-center link-content">
        <a :href="link" target="_blank"
            class="flex rounded-lg border border-indigo-600 bg-indigo-200 px-5 py-4 
            text-lg leading-6 font-medium shadow-md transition ease-in-out duration-150
            shadow-slate-400/50 
            hover:shadow-xl  hover:-translate-y-1 hover:scale-110 hover:bg-indigo-300 hover:shadow-indigo-400/50">
            <p class="mr-3 h-6 w-6">{{ icon }}</p>
            <h4 class="font-semibold text-violet-800">
                {{ text }}
            </h4>
            <div class="ml-auto mt-0.5 pl-4">
                <svg class="h-5 w-5 text-violet-800" xmlns="http://www.w3.org/2000/svg" fill="currentColor"
                    viewBox="0 0 20 20">
                    <path fill-rule="evenodd"
                        d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z" />
                </svg>
            </div>
        </a>
    </div>
</template>
<script setup>
    const {link, icon, text} = defineProps(['link', 'icon', 'text'])
</script>
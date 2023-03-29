<template lang="">
    <div class="container mx-auto flex flex-row flex-wrap">
        <div class="my-3 flex-row basis-full">
            <div class="text-center text-3xl font-bold text-cyan-700 basis-full flex-row">Esteban Fuentealba F.</div>
            <div class="text-center my-2">
                <Contact iconSize="h-6" showText="true" />
            </div>
        </div>
        <div class="bg-neutral-100 flex-row basis-full rounded-xl p-4 mx-2 mb-5">
            <div class="text-justify">
                <p class="text-md">
                    Welcome to my website/CV project, this app was created using 
                <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" href="https://github.com/vitejs/vite" target="_blank">viteJS</a> 
                and <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" href="https://vuejs.org/" target="_blank">vue.js</a> I hope you like it and found useful information about my professional career and qualifications.
                </p>
                <p>
                    This site is configured to automatically deploy through github actions using firebase as host, whenever is merged to <span class="text-red-500 font-semibold">main</span> branch.
                </p>
                <p>
                    Feel free to leave any comments on the <a href="https://github.com/ark4n631/vue-cv" class="font-medium text-blue-600 dark:text-blue-500 hover:underline" target="_blank">github repo</a> which this page will be hosted.
                </p>
                
            </div>
            <div class="rounded text-justify">
                This is a Single Web Application and it's stylized using <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" href="https://tailwindcss.com/">tailwind css</a>.
            </div>
        </div>
    </div>    
    <Overview />
    
</template>
<script>
import Contact from './Contact.vue';
import Overview from './Overview.vue';

export default {
    components: {
        Overview,
        Contact
    }
}
</script>

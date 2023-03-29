<template lang="">
    <div class="container mx-auto">
        <div class="my-10">
            <div class="text-center text-3xl font-bold text-cyan-700">Esteban Fuentealba F.</div>
            <div class="text-center my-2">
                <Contact />
            </div>
            
        </div>
        <div class="bg-neutral-100 rounded-xl p-5 my-5">
            <div class="text-justify">
                Welcome to my website/CV project, this app was created using 
                <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" href="https://github.com/vitejs/vite">viteJS</a> 
                and <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" href="https://vuejs.org/">vue.js</a> I hope you like it and found useful information about me and my career.

                Feel free to leave any comments on the github repo which this page will be hosted.
                <br/>
                <br/>
            </div>
            <div class="rounded text-justify">
                This is a Single Web Application and it's stylized using <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" href="https://tailwindcss.com/">tailwind css</a>
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

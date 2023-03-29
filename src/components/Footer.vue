<template>
    <div class="container flex">
        <div class="text-center basis-full">
            <Contact iconSize="h-6" :showText="false" />
            All rights reserved &copy; {{ new Date().getFullYear() }}
        </div>
        
    </div>
</template>
<script>
import Contact from './Contact.vue';


export default {
    components: {Contact}    
}
</script>

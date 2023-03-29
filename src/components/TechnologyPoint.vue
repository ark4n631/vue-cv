<template>
    <li>
        <img :src="tech.logo" :alt="tech.name" class="inline-block h-6 mr-2" />
        <a class="font-medium text-blue-600 dark:text-blue-500 hover:underline" :href="tech.url" target="_blank">
            {{ tech.name }}
        </a>
        
    </li>
</template>
<script>
export default {
    props: {
        tech: Object
    }
}
</script>

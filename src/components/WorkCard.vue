<template>
    <div class="bg-neutral-100 rounded-xl p-5 my-5">
        <div class="py-2 text-left text-cyan-700 text-2xl font-bold">
            {{ job.company }} - {{ job.location }}  <img v-if="job.flag" :src="job.flag" :alt="job.location" class="inline-block h-6 mr-2" />      
        </div>
        <div class="py-2 text-left text-md font-bold">
            {{ job.title }}
            ( {{ job.startDate }} - {{ job.endDate }} )
        </div>
        <div class="text-justify leading-8">
            {{ job.description }}
        </div>
        
        
    </div>
</template>
<script>
export default {
    props: {
        job: Object
    }
    
}
</script>

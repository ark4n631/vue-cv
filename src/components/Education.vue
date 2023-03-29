<template>
    <div class="container mx-auto my-auto">
        <div class="flex flex-row mx-5 my-5">
                <div class="text-center text-3xl font-semibold text-sky-800">Education</div>
            </div>
        <div class="mx-5 my-5 flex flex-row align-middle" v-for="course in courses">
            <div class="bg-neutral-100 rounded-xl p-5 my-5 mx-2">
                <div class="py-2 text-left text-cyan-700 text-2xl font-bold">
                {{ course.title }} at {{ course.institution }}        
            </div>
            <div class="py-2 text-left text-md font-bold">
                {{ course.location }}
                ( {{ course.startDate }} - {{ course.endDate }} )
            </div>
            <div class="text-justify leading-8">
                {{ course.description }}
            </div>
            
            </div>
        </div>
        <div class="my-auto flex flex-row mx-5 my-5">
                <div class="text-center text-3xl font-semibold text-sky-800">Certifications</div>
        </div>
        <div class="mx-5 my-auto flex flex-row my-5" v-for="certification in certifications">
            <div class="bg-neutral-100 rounded-xl p-5 my-5 mx-2 lg:w-100">
                <div class="py-2 text-left text-cyan-700 text-2xl font-bold">
                {{ certification.title }} at {{ certification.location }}        
            </div>
            <div class="py-2 text-left text-md font-bold">
                {{ certification.institution }} at {{ certification.certificationDate }} 
            </div>
            <div class="text-justify leading-8">
                {{ certification.description }}
            </div>
            
            </div>
        </div>
    </div>
        
</template>
<script>
export default {
    data () {
        return {
            courses: [
                {
                    institution: "Professional Institute Dr Virginio Gomez",
                    location: "Chillan, Chile",
                    title: "Bachelor in computer science and software development",
                    description: "Bachelor in computer science with mathematical bases and software development, including courses like: data structures, algorithms, relational databases, geo databases, artificial intelligence, software development, among other.",
                    startDate: "Mar 2008",
                    endDate: "Mar 2012"
                }
            ],
            certifications: [
                {
                    institution: "IETLS",
                    title: "IETLS",
                    location: "Sydney, Australia",
                    certificationDate: "23/02/2019",
                    description: "Report form Nº : 18AU013674FUEE468G"
                }
            ]
        }
    }
}
</script>

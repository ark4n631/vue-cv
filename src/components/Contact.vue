<template>
    <div class="container mx-auto p-3">
        <a href="mailto:estebanfuentealba@gmail.com" target="_blank">
            <img src="../assets/email.svg" class="inline-block mx-1" :class="[iconSize]" />
            <span v-show="showText">
                Email
            </span>
        </a>
        <a href="https://api.whatsapp.com/send?phone=+56951096894&text=Hello there" target="_blank">
            <img src="../assets/whatsapp.svg" class="inline-block mx-1" :class="[iconSize]" />
            <span v-show="showText">
                WhatsApp
            </span>
        </a>
        <a href="https://www.linkedin.com/in/ark4n631/" target="_blank">
            <img src="../assets/linkedin.svg" class="inline-block mx-1" :class="[iconSize]" />
            <span v-show="showText">
                Linkedin
            </span>
        </a>
        <a href="https://github.com/ark4n631" target="_blank">
            <img src="../assets/github.svg" class="inline-block mx-1" :class="[iconSize]" />
            <span v-show="showText">
                Github
            </span>
        </a>
        
    </div>
</template>
<script>
export default {
    props: {
        showText: Boolean,
        iconSize: String,
    }
}
</script>

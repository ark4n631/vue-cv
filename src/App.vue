<script setup>
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
import Footer from './components/Footer.vue';
import Router from './components/Router.vue';

const firebaseConfig = {
  apiKey: "AIzaSyBzA-pRuEs5C-zLUg_q46FrN08mQVsYu58",
  authDomain: "cv-vue-web.firebaseapp.com",
  projectId: "cv-vue-web",
  storageBucket: "cv-vue-web.appspot.com",
  messagingSenderId: "674207166012",
  appId: "1:674207166012:web:afa74f93a01a9ac6d59d39",
  measurementId: "G-KX43KBE57B"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);
</script>

<template>
  <Router />
  <Footer />
</template>

<style scoped>

</style>

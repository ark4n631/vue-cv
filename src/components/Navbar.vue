<template>
    <nav class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-sky-700 mb-3">
      <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
        <div v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="lg:flex lg:flex-grow items-center">
          <ul class="flex flex-col lg:flex-row list-none ml-auto">
            <li v-for="item in items" class="nav-item">
              <a class="mx-2 p-2 flex items-center text-md font-bold leading-snug text-white hover:opacity-75 rounded-2xl hover:bg-sky-400" :href="item.href" :class="isUrlActive(item.href) ? activeClass : ''">
                {{ item.name }} <img v-if="item.logo" :src="item.logo" :alt="item.name" class="inline-block h-6 mx-2" />
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    props: {
        items: Object,
        activeComponent: String
    },
    name: "blue-navbar",
    data() {
      return {
        showMenu: false,
        activeClass: "bg-sky-600"
      }
    },
    methods: {
      toggleNavbar: function(){
        this.showMenu = !this.showMenu;
      },
      isUrlActive: function(url){
        return url.replace('#', '') === this.activeComponent
      } 
    }
  }
  </script>
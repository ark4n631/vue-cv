<script>
import arrowDownLeftLogo from '../assets/arrowdownleft.svg'
import timerquarterLogo from '../assets/timequarter.svg'
import toolKitLogo from '../assets/toolkit.svg'
import diplomaLogo from '../assets/diploma.svg'
import Home from './Home.vue'
import NotFound from './NotFound.vue'
import Navbar from './Navbar.vue'
import WorkingHistory from './WorkingHistory.vue'
import Stack from './Stack.vue'
import Education from './Education.vue'

const routes = {
  '/': Home,
  '/workinghistory': WorkingHistory,
  '/technologies': Stack,
  '/education': Education
}

const routeMap = {
  '/': {
    name: 'Home',
    href: '#/',
    logo: arrowDownLeftLogo
  },
  '/workinghistory': {
    name: 'Working History',
    href: '#/workinghistory',
    logo: timerquarterLogo
  },
  '/technologies': {
    name: 'Technologies',
    href: '#/technologies',
    logo: toolKitLogo
  },
  '/education': {
    name: 'Education',
    href: '#/education',
    logo: diplomaLogo
  }
}

export default {
  components:{
    Navbar
  },
  data() {
    return {
      currentPath: window.location.hash,
      routes: routeMap
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    },
    currentUrl() {
      return this.currentPath.slice(1)
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
		  this.currentPath = window.location.hash
		})
  }
}
</script>

<template>
    <Navbar :items="routes" :activeComponent="currentUrl" showMenu="true" />
  <component :is="currentView" />
</template>

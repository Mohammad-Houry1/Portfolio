<template>
  <Navbar />
  <Home />
  <div
    v-for="component in components"
    :key="component.name"
    class="min-h-screen m-y-auto flex justify-center items-center bg-blek max-sm:py-28 max-md:py-32"
    :ref="component.name"
  >
    <component :is="component.componentName" />
  </div>
  <Contact />
</template>
<script setup>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Contact from './components/contact.vue'

const components = [
  { name: 'about', componentName: About },
  { name: 'projects', componentName: Projects }
]
</script>

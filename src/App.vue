<script setup>
import { ref } from 'vue';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import TentangKami from './components/TentangKami.vue';
import MemilihKami from './components/MemilihKami.vue';
import Product from './components/Product.vue';
import Dokumentasi from './components/Dokumentasi.vue';
import HubungiKami from './components/HubungiKami.vue';
import Footer from './components/Footer.vue';
import Whatsapp from './components/Whatsapp.vue';

const activeSection = ref('hero');
const setActiveSection = (sectionId) => {
  activeSection.value = sectionId;
};
</script>

<template>
  <Navbar :activeSection="activeSection" />

  <main>
    <Hero @setActiveSection="setActiveSection" />
    <TentangKami @setActiveSection="setActiveSection" />
    <MemilihKami />
    <Product @setActiveSection="setActiveSection" />
    <Dokumentasi @setActiveSection="setActiveSection" />
    <HubungiKami @setActiveSection="setActiveSection" />
    <Footer />
    <Whatsapp />
  </main>
</template>

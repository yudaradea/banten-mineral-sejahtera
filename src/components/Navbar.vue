<script setup>
import { ref, onMounted } from 'vue';
import LogoAja from '../assets/images/LogoAja.png';

const isOpen = ref(false);
const scrollPosition = ref(true);

const handleScroll = () => {
  if (window.scrollY > 1) {
    scrollPosition.value = false;
  } else {
    scrollPosition.value = true;
  }
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});
</script>

<template>
  <transition
    v-show="scrollPosition"
    enter-active-class="duration-500 ease-out"
    enter-from-class="transform -translate-y-full opacity-0"
    enter-to-class="opacity-100"
    leave-active-class="duration-500 ease-in"
    leave-from-class="opacity-100 "
    leave-to-class="transform -translate-y-full opacity-0"
  >
    <div class="py-3 border-b bg-primary">
      <div
        class="container flex flex-col items-center justify-around gap-2 text-sm font-semibold md:flex-row text-slate-700"
      >
        <div class="flex items-center gap-1">
          <i class="text-base fa-solid fa-envelope mt-[1px]"></i>
          <p>cvbantenminerals@gmail.com</p>
        </div>
        <div class="flex items-center gap-1">
          <i class="text-base fa-solid fa-phone mt-[1px]"></i>
          <p>087772333634</p>
        </div>
      </div>
    </div>
  </transition>

  <header
    class="sticky top-0 z-50 py-4 bg-white border-b shadow-sm rounded-b-2xl"
  >
    <nav class="container flex items-center justify-between">
      <div class="">
        <a href="/" class="flex items-center gap-2">
          <img :src="LogoAja" alt="" class="w-7 md:w-8" />
          <span class="text-3xl font-semibold md:text-4xl">BMS</span>
        </a>
      </div>
      <div
        class="items-center hidden gap-6 text-sm font-semibold tracking-wide xl:gap-8 lg:flex text-slate-400"
      >
        <a href="" class="active">Home</a>
        <a href="" class="transition-all duration-200 hover:text-primary"
          >Tentang Kami</a
        >
        <a href="" class="transition-all duration-200 hover:text-primary"
          >Produk Material</a
        >
        <a href="" class="transition-all duration-200 hover:text-primary"
          >Galeri</a
        >
        <a href="" class="transition-all duration-200 hover:text-primary"
          >Hubungi Kami</a
        >
      </div>
      <div class="flex cursor-pointer lg:hidden" @click="isOpen = !isOpen">
        <div v-show="!isOpen">
          <i class="text-2xl fa-solid fa-bars"></i>
        </div>
        <div v-show="isOpen">
          <i class="text-2xl fa-solid fa-x"></i>
        </div>
      </div>
    </nav>
    <!-- Mobile Menu -->
    <transition
      class="pt-4 pb-8 shadow-md rounded-b-2xl"
      v-show="isOpen"
      enter-active-class="duration-500 ease-out"
      enter-from-class="transform -translate-y-full opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="duration-500 ease-in"
      leave-from-class="opacity-100 "
      leave-to-class="transform -translate-y-full opacity-0"
    >
      <div
        class="container z-30 flex flex-col pt-2 text-sm font-semibold bg-white lg:hidden"
      >
        <a
          href=""
          @click="isOpen = !isOpen"
          class="py-3 border-b-2 active border-primary"
          >Home</a
        >
        <a
          href=""
          @click="isOpen = !isOpen"
          class="py-3 transition-all duration-200 border-b-2 hover:text-primary border-primary"
          >Tentang Kami</a
        >
        <a
          href=""
          @click="isOpen = !isOpen"
          class="py-3 transition-all duration-200 border-b-2 hover:text-primary border-primary"
          >Produk Material</a
        >
        <a
          href=""
          @click="isOpen = !isOpen"
          class="py-3 transition-all duration-200 border-b-2 hover:text-primary border-primary"
          >Galeri</a
        >
        <a
          href=""
          @click="isOpen = !isOpen"
          class="py-3 transition-all duration-200 border-b-2 hover:text-primary border-primary"
          >Hubungi Kami</a
        >
      </div>
    </transition>
  </header>
</template>

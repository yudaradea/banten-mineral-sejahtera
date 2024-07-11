<script setup>
import LogoAja from "../assets/images/LogoAja.png";
</script>

<template>
  <div class="py-3 border-b bg-primary">
    <div class="container flex justify-around text-sm italic font-semibold text-slate-700">
      <h1 class="">Banten Mineral Sejahtera</h1>
      <div class="flex items-center gap-1">
        <i class="fa-solid fa-phone"></i>
        <p>087772333634</p>
      </div>
    </div>
  </div>
  <Header class="py-4 sticky top-0 shadow-sm border-b">
    <nav class="flex justify-between items-center container">
      <div class="">
        <a href="/" class="flex items-center gap-2">
          <img :src="LogoAja" alt="" class="w-7 md:w-8" />
          <span class="text-3xl md:text-4xl font-semibold">BMS</span>
        </a>
      </div>
      <div class="items-center gap-6 hidden lg:flex text-sm tracking-wide font-semibold text-slate-400">
        <a href="" class="active">Home</a>
        <a href="" class="hover:text-primary transition-all duration-200">Tentang Kami</a>
        <a href="" class="hover:text-primary transition-all duration-200">Produk Material</a>
        <a href="" class="hover:text-primary transition-all duration-200">Galeri</a>
        <a href="" class="hover:text-primary transition-all duration-200">Hubungi Kami</a>
      </div>
      <div class="flex lg:hidden"></div>
    </nav>
  </Header>
</template>

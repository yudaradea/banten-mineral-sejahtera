<script setup>
import Title from "./Title.vue";
</script>

<template>
  <section id="contactUs" ref="contactUs" class="pt-10 pb-12 bg-primary md:pt-12 md:pb-14 lg:pt-14 lg:pb-16 border-b-2">
    <div class="container grid grid-cols-1 gap-2">
      <Title :title="'Connect With Us'" />
    </div>
    <div class="container grid lg:grid-cols-2 lg:place-items-center gap-8 mt-2 lg:mt-6">
      <div class="mt-6 lg:mt-8 space-y-4">
        <div class="flex items-start gap-4 md:text-lg">
          <i class="fa-solid text-2xl fa-phone"></i>
          <span class="font-semibold">087772333634 (Office)</span>
        </div>
        <div class="flex items-start gap-4 md:text-lg">
          <i class="fa-solid text-2xl fa-envelope"></i>
          <span class="font-semibold">cvbantenminerals@gmail.com</span>
        </div>
        <div class="flex items-start gap-4 md:text-lg">
          <i class="fa-solid text-2xl fa-location-dot"></i>
          <span class="font-semibold">Jl. Siliwangi KP. Jaura RT. 002 RW. 002 Rangkasbitung Timur, Kec. Rangkasbitung, Kab. Lebak, Provinsi Banten.</span>
        </div>
      </div>
      <div>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15860.95303000204!2d106.24494983476482!3d-6.363203022379457!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e42112b82f4aa29%3A0x2a9c4cf2496990d5!2sKp.%20Jaura%2C%20West%20Rangkasbitung%2C%20Rangkasbitung%2C%20Lebak%20Regency%2C%20Banten!5e0!3m2!1sen!2sid!4v1721278940203!5m2!1sen!2sid"
          class="rounded-xl w-[350px] lg:w-[600px] md:w-full h-[350px] lg:h-[450px]"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>
    </div>
  </section>
</template>

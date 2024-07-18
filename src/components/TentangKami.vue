<script setup>
import { ref, defineEmits, onUnmounted } from 'vue';
import Title from './Title.vue';
import VisiMisi from './VisiMisi.vue';

const section = ref(null);
const emit = defineEmits(['setActiveSection']);

const handleScroll = () => {
  if (
    section.value &&
    section.value.getBoundingClientRect().top < window.innerHeight / 2
  ) {
    emit('setActiveSection', 'tentangKami');
  }
};

window.addEventListener('scroll', handleScroll);

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <section
    id="tentangKami"
    ref="section"
    class="py-12 bg-gray-100 md:py-14 lg:py-16"
  >
    <Title :title="'Tentang Kami'" />
    <div
      class="container grid items-center gap-6 pt-8 lg:grid-cols-2 md:pt-10 lg:pt-14"
    >
      <div class="order-2 pt-2 lg:order-1 lg:pt-0">
        <h1 class="font-bold uppercase md:text-2xl">Company History</h1>
        <p
          class="py-2 text-sm leading-relaxed text-justify md:text-base md:leading-relaxed"
        >
          Secara resmi perusahaan ini berdiri dengan nama
          <span class="font-bold">CV. BANTEN MINERAL SEJAHTERA</span> . Banten
          Mineral Sejahtera perusahaan Raw Material Supplier yang memiliki
          pengalaman dan kompetensi di bidangnya, serta mampu mengikuti
          perkembangan teknologi sebagai standar prosesnya. Selain menyediakan
          material beton dan produk konstruksi berkualitas tinggi, Banten
          Mineral Sejahtera juga mengandalkan sumber daya manusia yang
          profesional untuk memberikan pelayanan terbaik guna menjamin kepuasan
          pelanggan.
        </p>
        <p
          class="text-sm leading-relaxed text-justify md:text-base md:leading-relaxed"
        >
          <span class="font-bold">Banten Mineral Sejahtera</span> mengelola
          bisnisnya dengan profesional dan didukung oleh keterampilan manajemen
          yang andal. Seiring perkembangan zaman dan sesuai dengan visi dan misi
          perusahaan, Banten Mineral Sejahtera akan terus berinovasi demi
          menjadi perusahaan Raw Material Supplier yang lebih andal dan mampu
          menjangkau pasar nasional.
        </p>

        <div class="pt-6">
          <div class="h-2 bg-primary rounded-t-xl"></div>
          <div
            class="flex flex-col items-center px-[12px] py-4 pb-6 bg-primary/40 rounded-b-xl shadow-sm"
          >
            <div class="w-full italic">
              <p class="text-[13px] leading-relaxed text-justify">
                Hingga saat ini Banten Mineral Sejahtera telah menjalin kerja
                sama dengan berbagai pihak, baik pemerintah maupun
                non-pemerintahan, dan meyakini bahwa peluang bisnis di bidang
                penyediaan bahan baku cukup baik, berkelanjutan dan berjangka
                panjang.
              </p>
              <p class="text-[13px] leading-relaxed text-justify pt-2">
                Hal ini di sebabkan oleh terus meningkatnya kebutuhan akan bahan
                baku beton dan material bangunan di bidang konstruksi karena
                merupakan bahan utama konstruksi. Sebagai perusahaan yang
                bergerak di bidang ini, perusahaan akan terus berkomitmen untuk
                lebih mengembangkan bisnis dengan model kerja dan kerjasama yang
                baik dan tepat guna sehingga dapat memberikan manfaat bagi semua
                pihak yang terlibat.
              </p>
            </div>
          </div>
        </div>
      </div>
      <div
        class="w-full h-[400px] md:h-[550px] lg:h-[650px] overflow-hidden rounded-tr-[36px] rounded-bl-[36px] lg:w-5/6 lg:justify-self-end order-1 lg:order-2 pt-2 lg:pt-0"
      >
        <img
          src="../assets/images/tentangKami.jpg"
          alt=""
          class="object-cover w-full h-full transition-all duration-500 hover:scale-105 rounded-tr-[36px] rounded-bl-[36px]"
        />
      </div>
    </div>

    <VisiMisi />
  </section>
</template>

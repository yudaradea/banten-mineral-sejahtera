<script setup>
import { ref } from "vue";
import Title from "./Title.vue";
import Modal from "./Modal.vue";
import products from "../data/product.json";
import Sertifikat from "./Sertifikat.vue";

const isOpenModal = ref(false);
const modalData = ref({});
function showModal(product) {
  isOpenModal.value = true;
  modalData.value = product;
  document.body.classList.add("no-scroll");
}
function closeModal() {
  isOpenModal.value = false;
  document.body.classList.remove("no-scroll");
}

function getImageUrl(img) {
  return new URL(`../assets/images/${img}`, import.meta.url).href;
}
</script>

<template>
  <section id="product" ref="product" class="pt-10 pb-12 bg-gray-100 md:pt-12 md:pb-14 lg:pt-14 lg:pb-16">
    <Title :title="'Produk Material'" />

    <div class="container grid grid-cols-2 mt-8 gap-x-4 gap-y-6 md:mt-10 md:grid-col-3 lg:grid-cols-4">
      <div v-for="product in products" :key="product.id" class="relative flex flex-col border-2 rounded-lg shadow-sm border-primary">
        <i class="absolute text-4xl -top-2 left-2 md:left-3 fa-solid fa-bookmark text-primary"></i>
        <img :src="getImageUrl(product.img)" alt="product" class="object-cover w-full h-[150px] md:h-[300px] rounded-t-lg" />
        <p class="px-2 pt-5 pb-3 font-semibold text-center">
          {{ product.title }}
        </p>
        <div class="flex items-center justify-center w-full py-2 mt-auto mb-4">
          <button class="px-4 py-1.5 text-sm shadow-sm border border-primary rounded-md bg-primary hover:bg-transparent hover:shadow-md transition-all duration-300 font-medium" @click="showModal(product)">
            <i class="cursor-pointer fa-solid fa-eye"></i>

            Detail
          </button>
        </div>
      </div>
    </div>

    <!-- Modal -->
    <Modal :isOpen="isOpenModal" :modalData="modalData" @closeModal="closeModal" />

    <Sertifikat />
  </section>
</template>

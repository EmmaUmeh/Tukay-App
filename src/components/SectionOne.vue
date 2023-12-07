<script setup>
defineProps({
    text: String,
})
import GuySapa from "../../public/guy_sapa.png";
import LadySapa from "../../public/lady_sapa.png";
import IgreetBros from "../../public/greet_bros.png";
import CustomModal from './CustomModal.vue';


const sectionlist = [
  {
    id: 0,
    ImageUrl: GuySapa,
    title: "No more Sapa",
    content: "In Nigerian Pidgin English, Sapa is sometimes used to describe financial hardship or running out of money.",
  },
  {
    id: 1,
    ImageUrl: LadySapa,
    title: "Beg",
    content: "In Nigerian Pidgin English, Sapa is sometimes used to describe financial hardship or running out of money.",
  },
  {
    id: 2,
    ImageUrl: IgreetBros,
    title: "Send Money",
    content: "In Nigerian Pidgin English, Sapa is sometimes used to describe financial hardship or running out of money.",
  },
];
</script>

<template>
    <div class="mt-5 mb-5">
        <div class="flex flex-col items-center justify-center">
            <h3 class="text-3xl sm:text-lg md:lg font-bold mb-2 flex items-center justify-center">{{ text }}</h3>
            <p class="text-lg font-semibold mb-3 w-5/12 flex items-center justify-center">This is how our products works</p>
        </div>

        <CustomModal>
        <div v-for="item in sectionlist" :key="item.id" class="bg-white flex flex-col  items-center mb-5 py-5 px-5 rounded-md">
            <img :src="item.ImageUrl" alt="Section Image" class="w-24 object-cover rounded-full" />
            <h3 class="text-xl font-bold mt-3">{{ item.title }}</h3>
            <p class="text-base text-gray-600">{{ item.content }}</p>
        </div>
    </CustomModal>
        
    </div>
</template>
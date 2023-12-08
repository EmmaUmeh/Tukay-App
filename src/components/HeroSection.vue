<script setup>
import CustomButton from '../components/CustomButton.vue';
import SettingsImage from '../../public/settings.png';
</script>

<template>
  <div class="w-50 py-36 px-20">
    <div>
      <h3 class="text-6xl font-semibold mb-2 ">Get your urgent 2k</h3>
      <p class="text-lg font-semibold mb-3 w-5/12 sm:w-full md:w-full">No cash, No wahala get our application and deal with Sapa.</p>
    </div>

    <div class="flex items-center gap-8 mb-4">
      <div class="flex flex-col">
        <span class="text-[#000000] font-semibold">20k +</span>
        <span class="text-xs">Active users</span>
      </div>

      <div class="flex flex-col">
        <span class="text-[#000000] font-semibold">30M +</span>
        <span class="text-xs">Download</span>
      </div>
    </div>

    <div class="flex items-center gap-6">
      <CustomButton text="Get Started" class="bg-primary text-white sm:text-xs md:text-xs rounded-lg px-5 py-2"></CustomButton>

      <div class="flex items-center gap-2">
        <img :src="SettingsImage" width="18%"/>
        <span>How it Works</span>
      </div>
    </div>
  </div>
</template>

<style>
@media (min-width: 768px) {
  .w-50 {
    background-image: url('../../public/herologo.png');
    background-position: right;
    background-repeat: no-repeat;
    background-size: contain;
    height: 80vh;
  }
}
</style>

<script setup>
import TukayLogo from '../../public/logo.png'
import CustomButton from '../components/CustomButton.vue'
import VueFeather from 'vue-feather';

import { ref } from 'vue';

const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

</script>

<template>
   <nav class="">
      <div class="sm:hidden md:hidden block">
         <ul class="flex items-center justify-around">
            <div>
               <li>
                  <img :src="TukayLogo" alt="TukayLogo" />
               </li>
            </div>


            <div class="flex items-center gap-7 font-semibold">
               <li class="text-[#000000]">Home</li>
               <li class="text-[#474747]">Services</li>
               <li class="text-[#474747]">Features</li>
               <li class="text-[#474747]">Contact</li>
            </div>

            <div class="flex items-center gap-8">
               <li>
                  <CustomButton text="Login" class="bg-primary text-white rounded-lg  px-6 py-1"></CustomButton>
               </li>

               <li>
                  <CustomButton text="Sign up"
                     class="text-primary font-semibold bg-secondary border border-[#00545F] rounded-lg  px-6 py-1">
                  </CustomButton>
               </li>
            </div>

         </ul>
      </div>


      <!-- mobile responsive -->

      <div class="sm:block md:block hidden">
         <ul class="flex items-center justify-around">
            <div>
               <li>
                  <img :src="TukayLogo" alt="TukayLogo" />
               </li>
            </div>

            <transition name="fade">
          <div v-if="isMobileMenuOpen" class="mobile-menu">
            <div class="flex flex-col items-center gap-7 font-semibold">
              <li class="text-[#000000]">Home</li>
              <li class="text-[#474747]">Services</li>
              <li class="text-[#474747]">Features</li>
              <li class="text-[#474747]">Contact</li>
            </div>

            <div class="flex flex-col items-center gap-8 mt-4">
              <li>
                <CustomButton text="Login" class="bg-primary text-white rounded-lg px-6 py-1"></CustomButton>
              </li>

              <li>
                <CustomButton text="Sign up" class="text-primary font-semibold bg-secondary border border-[#00545F] rounded-lg px-6 py-1"></CustomButton>
              </li>
            </div>
          </div>
        </transition>

               <div class="cursor-pointer z-50">
                  <VueFeather
          v-if="!isMobileMenuOpen"
          @click="toggleMobileMenu"
          type="menu"
          size="32"
        />
        <VueFeather
          v-if="isMobileMenuOpen"
          @click="toggleMobileMenu"
          type="x"
          size="32"
        />
               </div>
         </ul>
      </div>


   </nav></template>


<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}


.mobile-menu {
  position: absolute;
  top: 2rem;
  background-color: #EBFFB7; /* Adjust as needed */
  width: 100%;
  padding: 2rem;
  z-index: 50;
}
</style>

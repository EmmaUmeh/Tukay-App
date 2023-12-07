<script setup>
import CustomButton from '../components/CustomButton.vue';
import Currency from '../../public/money.png';


</script>



<template>
    <div class="bg-secondary">
       <div class="flex items-center sm:flex-col md:flex-col justify-between pl-20  py-3">
            <div class="pt-5">
                <h3 class="text-3xl sm:text-2xl md:2xl font-semibold mb-2">Urgent Tukay- the Notes</h3>
                <p class="text-lg font-semibold mb-3 w-11/12 sm:w-full md:w-full">No cash, No wahala get our application and deal with Sapa.</p>
                <CustomButton text="Get Started" class="bg-primary text-white rounded-lg w-40 text-center px-5 py-2"></CustomButton>
            </div>

            <div class="">
                
                <div>
                    <img :src="Currency" width="90%"/>
                </div>
            </div>
       </div>
    </div>
</template>
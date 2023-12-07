<script setup>
import Sectionbanner from '../../public/sectionbannerTwo.png'
import IgreetBros from "../../public/greet_brosbigimage.png";
</script>


<template>
    <div class="flex justify-between bg-primary">

       <div>
        <img :src="IgreetBros" width="90%"/>
       </div>

        <div >
            <img :src="Sectionbanner" width="90%" />
        </div>
    </div>
</template>
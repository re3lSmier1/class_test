<script setup>

import Navbar from "@/components/navbar.vue";
import Carousel from "@/components/carousel.vue"
import ImageCards from "@/components/ImageCards.vue";
import {ref} from "vue";
let dishes = ref([
  { name: "Allisa", description: "description 1", image: "/bird-9376831_640.jpg" },
  { name: "Mandy", description: "description 2", image: "/canal-9182536_1280.jpg" },
  { name: "Nickesha", description: "description 3", image: "/losangeles-7754986_1280.jpg" },
])

let studentNames = ref([
    "Nickesha", "Allisa", "Vernal", "Rihann", "Mandy"
])
</script>

<template>
  <div>
    <Navbar />
    <Carousel />
     <br><br><br>
     <br><br><br>
    <div>
      <span style="margin-right: 15px" v-for="(name, index) in studentNames">{{ name }} {{ index +1 }}</span>
    </div>
    <div class="row">

        <ImageCards v-for="(dish, index) in dishes" v-if="index !== 2"
                    :name="dish.name"
                     :description="dish.description"
                     :image-url="dish.image"
        />

    </div>
    This is our home page
  </div>
</template>

<style scoped>

</style>
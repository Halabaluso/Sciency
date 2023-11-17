<template>
  <div class="hero min-h-screen bg-hero" style="background-image: url(https://www.freecodecamp.org/news/content/images/2022/09/jonatan-pie-3l3RwQdHRHg-unsplash.jpg);">
    <div class="bg-opacity-60"></div>
        <div class="hero-content text-center text-neutral-content pt-32"> 
            <div class="max-w-md">
                <div class="mb-5 hover:scale-110 duration-300">
                    <button class="btn bg-gradient-to-tr to-purple-700 from-pink-500 border-none text-white">UPCOMING NEW {{ data.year }} EVENT</button>
                </div>
            <p class="text-xl mb-2">Participate in the biggest event</p>
            <h1 class="mb-5 text-5xl font-extrabold">THE LARGEST SCIENCE EVENT IN THE WORLD</h1>
            <div class="flex flex-row justify-between items-center text-white font-bold text-xl">
                <p class="text-xl"><Icon name="mdi:earth" size = "1.5em" class="text-pink-500"/> Madrid, Spain</p>
                <p class="text-xl"><Icon name="mdi:calendar" size = "1.5em" class="text-pink-500"/> {{ data.date }}</p>
            </div>
            </div>
            
        </div>
    </div>
</template>

<script setup>
import moment from "moment"
    const data = reactive({
        date: moment().add(7, "days").format("MM-DD-YYYY, HH:mm"),
        year: moment().format("YYYY")
    })
</script>

<style>

</style>
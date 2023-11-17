<template>
    <div class="hero min-h-screen">
        <div class="hero-content mt-20">
            <div>
                <p class="mb-2uppercase text-center uppercase text-purple-500">conferences</p>
                <h1 class="text-5xl font-bold uppercase text-center">Conferences and schedules.</h1>
                <div class="flex flex-row items-center justify-between mt-10">
                    <div @click="changeEvents(1)" id = "button1" class="flex flex-row items-center bg-gray-100 p-5 m-2 hover:scale-110 hover:-translate-y-2 duration-300 text-pink-500 border-2">
                        <Icon name="mdi:calendar" size="3em"/>
                        <div class="ml-4">
                            <p class="font-bold">{{ data.date }} </p>
                            <p class="text-xs">CONFERENCES AND SCHEDULES</p>
                        </div>
                    </div>
                    <div @click="changeEvents(2)" id = "button2" class="flex flex-row items-center bg-gradient-to-tr from-pink-500 to-purple-500 text-white p-5 m-2 hover:scale-110 hover:-translate-y-2 duration-300">
                        <Icon name="mdi:calendar" size="3em"/>
                        <div class="ml-4">
                            <p class="font-bold">{{ data.date1 }} </p>
                            <p class="text-xs">CONFERENCES AND SCHEDULES</p>
                        </div>
                    </div>
                    <div @click="changeEvents(3)" id = "button3" class="flex flex-row items-center bg-gradient-to-tr from-pink-500 to-purple-500 text-white p-5 m-2 hover:scale-110 hover:-translate-y-2 duration-300">
                        <Icon name="mdi:calendar" size="3em"/>
                        <div class="ml-4">
                            <p class="font-bold">{{ data.date2 }} </p>
                            <p class="text-xs">CONFERENCES AND SCHEDULES</p>
                        </div>
                    </div>
                    <div @click="changeEvents(4)" id = "button4" class="flex flex-row items-center bg-gradient-to-tr from-pink-500 to-purple-500 text-white p-5 m-2 hover:scale-110 hover:-translate-y-2 duration-300">
                        <Icon name="mdi:calendar" size="3em"/>
                        <div class="ml-4">
                            <p class="font-bold">{{ data.date3 }} </p>
                            <p class="text-xs">CONFERENCES AND SCHEDULES</p>
                        </div>
                    </div>
                </div>
                <div class="flex flex-col bg-gray-100 m-2">
                    <div class="flex flex-row items-center border-b pb-5 border-gray-200 mx-5 bg-white p-10 mt-5">
                        <div class="avatar">
                            <div class="w-36 mask mask-hexagon">
                                <img src="../img/vendor1.jpg" />
                            </div>
                        </div>
                        <div class="ml-10">
                            <p class="font-bold text-purple-500"><Icon name="mdi:clock-time-seven-outline" size = "1.5em"></Icon> 10:00 - 11:00</p>
                            <p class="font-extrabold my-2 text-xl">Exploring the Cosmos: Recent Discoveries in Astrophysics</p>
                            <p class="text-pink-500">By: Dr. Olivia Harrington</p>
                        </div>
                    </div>
                    <div class="flex flex-row items-center border-b pb-5 border-gray-200 mx-5 bg-white p-10">
                        <div class="avatar">
                            <div class="w-36 mask mask-hexagon">
                                <img src="../img/vendor2.jpg" />
                            </div>
                        </div>
                        <div class="ml-10">
                            <p class="font-bold text-purple-500"><Icon name="mdi:clock-time-seven-outline" size = "1.5em"></Icon> 10:00 - 11:00</p>
                            <p class="font-extrabold my-2 text-xl">Unlocking the Brain's Secrets: A Journey into Neurogenetics</p>
                            <p class="text-pink-500">By: Prof. Ethan Montgomery</p>
                        </div>
                    </div>
                    <div class="flex flex-row items-center border-b pb-5 border-gray-200 mx-5 bg-white p-10">
                        <div class="avatar">
                            <div class="w-36 mask mask-hexagon">
                                <img src="../img/vendor3.jpg" />
                            </div>
                        </div>
                        <div class="ml-10">
                            <p class="font-bold text-purple-500"><Icon name="mdi:clock-time-seven-outline" size = "1.5em"></Icon> 12:00 - 14:00</p>
                            <p class="font-extrabold my-2 text-xl">Sustainability Economics: Balancing Profit and the Planet</p>
                            <p class="text-pink-500">By: Dr. Penelope Reynolds</p>
                        </div>
                    </div>
                    <div class="flex flex-row items-center border-b pb-5 border-gray-200 mx-5 bg-gradient-to-tr to-pink-500 from-purple-500 p-10 text-white">
                        <div class="avatar">
                            <div class="w-36 mask mask-hexagon">
                                <img src="../img/vendor4.jpg" />
                            </div>
                        </div>
                        <div class="ml-10">
                            <p class="font-bold "><Icon name="mdi:clock-time-seven-outline" size = "1.5em"></Icon> 17:00 - 19:00</p>
                            <p class="font-extrabold my-2 text-xl">Genetic Engineering for a Healthier Future</p>
                            <div>
                                <div class="rating rating-sm">
                                <input type="radio" name="rating-6" class="mask mask-star-2 bg-orange-400" />
                                <input type="radio" name="rating-6" class="mask mask-star-2 bg-orange-400" />
                                <input type="radio" name="rating-6" class="mask mask-star-2 bg-orange-400" />
                                <input type="radio" name="rating-6" class="mask mask-star-2 bg-orange-400" />
                                <input type="radio" name="rating-6" class="mask mask-star-2 bg-orange-400" checked />
                                </div>
                            </div>
                            <p class="">By: Dra. Isabella Drake</p>
                        </div>
                    </div>
                    <div class="flex flex-row items-center border-b pb-5 border-gray-200 mx-5 bg-white p-10 mb-5">
                        <div class="avatar">
                            <div class="w-36 mask mask-hexagon">
                                <img src="../img/vendor5.jpg" />
                            </div>
                        </div>
                        <div class="ml-10">
                            <p class="font-bold text-purple-500"><Icon name="mdi:clock-time-seven-outline" size = "1.5em"></Icon> 10:00 - 11:00</p>
                            <p class="font-extrabold my-2 text-xl">Exploring the Cosmos: Recent Discoveries in Astrophysics</p>
                            <p class="text-pink-500">By: Dr. Olivia Harrington</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import moment from "moment"
const data = reactive({
    date: moment().format("DD-MM-YYYY, HH:mm"),
    date1: moment().add(1, "days").format("DD-MM-YYYY, HH:mm"),
    date2: moment().add(2, "days").format("DD-MM-YYYY, HH:mm"),
    date3: moment().add(3, "days").format("DD-MM-YYYY, HH:mm"),
    lastbutton: 1
})

const changeEvents = (i) => {
    const element = document.querySelector("#button" + i)
    element.classList.remove("bg-gradient-to-tr")
    element.classList.add("bg-bg-gray-100")
    element.classList.remove("text-white")
    element.classList.add("text-pink-500")
    element.classList.add("border")

    const element1 = document.querySelector("#button" + data.lastbutton)
    element1.classList.add("bg-gradient-to-tr")
    element1.classList.add("from-pink-500")
    element1.classList.add("to-purple-500")
    element1.classList.add("text-white")
    element1.classList.remove("bg-bg-gray-100")
    element1.classList.remove("text-pink-500")
    element1.classList.remove("border")
    data.lastbutton = i
}
</script>

<style></style>
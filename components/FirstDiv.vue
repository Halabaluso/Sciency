<template>
    <div class="hero min-h-screen bg-hero" style="
              background-image: url(https://i.pinimg.com/originals/a9/02/c3/a902c36ba47e99e7330ff4ced84f7425.jpg);
            ">
        <div class="hero-overlay bg-gradient-to-tr from-pink-500/80 to-purple-500/80 bg-opacity-60"></div>
        <div class="hero-content text-center text-neutral-content py-20">
            <div class="max-w-xl text-white">
                <p class="text-xl mb-2 font-bold">Tickets almost sold out</p>
                <h1 class="mb-5 text-5xl font-extrabold">BUY YOUR TICKET.</h1>
                <p>
                    Join us for this exciting scientific event in the heart of Madrid,
                    Spain. Secure your spot by purchasing your tickets now.
                </p>
                <div class="flex flex-row justify-between items-center">
                    <div class="border border-4 border-white p-5 m-2 w-32">
                        <p class="font-bold text-4xl">0{{ data.days }}</p>
                        <p>Days</p>
                    </div>
                    <div class="border border-4 border-white p-5 m-2 w-32">
                        <p class="font-bold text-4xl">{{ data.hours }}</p>
                        <p>Hours</p>
                    </div>
                    <div class="border border-4 border-white p-5 m-2 w-32">
                        <p class="font-bold text-4xl">{{ data.minutes }} </p>
                        <p>Minutes</p>
                    </div>
                    <div class="border border-4 border-white p-5 m-2 w-32">
                        <p class="font-bold text-4xl">{{ data.seconds }} </p>
                        <p>Seconds</p>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<script setup>
import moment from "moment"
const data = reactive({
    days: moment().add(7, "days").format("DD"),
    hours: moment("12:00", "HH:mm").add(7, "days").format("HH"),
    minutes: moment("12:00", "HH:mm").add(7, "days").format("mm"),
    seconds: moment("12:00:00", "HH:mm:ss").add(7, "days").format("ss")
})

onMounted(() => {
    const todayDays = moment().format("DD")
    data.days = data.days - todayDays

    const todayHours = moment().format("HH")
    data.hours = data.hours - todayHours

    const todayMinutes = moment().format("mm")
    data.minutes = todayMinutes - data.minutes
    if(data.minutes < 10){
        data.minutes = "0" + data.minutes
    }
    
    let todaySeconds = moment().format("ss")
    data.seconds = todaySeconds - data.seconds

    setInterval(() => {
        data.seconds = parseInt(data.seconds) - 1
        if(parseInt(data.seconds) < 10){
            data.seconds = "0" + data.seconds
            if(parseInt(data.seconds) == 0){
                data.seconds = 60
                data.minutes = parseInt(data.minutes) - 1
                if(parseInt(data.minutes) < 10){
                    data.minutes = "0" + data.minutes
                    if(parseInt(data.minutes) == 0){
                        data.minutes = 60
                    }
                }
            }
        }
    }, 1000)

})
</script>

<style></style>
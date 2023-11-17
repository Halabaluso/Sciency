<template>
    <div class="hero min-h-screen"
        style="background-image: url(https://images-eur.cvent.com/pr53/6a03f092600d4fd7b17308d9c0fb8bf9/beedfc5e5aa6bb934a4c6bccef6608ea/7fd7380177ad4c92a0916df31d1e07e0/9e7730605ddb469c14a53fa7a925f670!_!5efa45f3e4ce3801b26349988b74b909.jpeg?f=webp);">
        <div class="hero-overlay bg-opacity-60"></div>
        <div>
            <div class="flex flex-col items-center">
                <button onclick="my_modal_1.showModal()"
                    class="bg-gradient-to-tr from-pink-500 to-purple-500 rounded-full p-2 shadow-lg hover:from-purple-500 hover:to-pink-500 duration-300 hover:scale-110 hover:-translate-y-2">
                    <Icon name="mdi:play-circle-outline" size="6em" color="white"></Icon>
                </button>
                <div class="text-white text-center max-w-md mt-5">
                    <h1 class="mb-5 text-5xl font-bold uppercase">Discover everything that awaits you.</h1>
                    <p class="mb-5">The largest scientific event in Spain that brings together the most emblematic
                        international professionals in the world.</p>
                </div>
            </div>
        </div>
    </div>
    <dialog id="my_modal_1" class="modal">
        <div class="modal-box bg-transparent w-11/12 max-w-5xl h-5/6">
            <form method="dialog">
                <button @click="takeIframe" class="btn btn-sm btn-circle btn-ghost absolute right-2 top-2 bg-white">✕</button>
            </form>
            <iframe v-if="!boolean" width="100%" height="100%" src="https://www.youtube.com/embed/aSb4CWJZITo" frameborder="0" encrypted-media allowfullscreen></iframe>
        </div>
    </dialog>
</template>

<script setup>
const data = reactive({
    boolean: false
})

const takeIframe = () => {
    if(data.boolean === false){
        data.boolean = true
    }else{
        data.boolean = false
    }
}
</script>

<style></style>
<template>
  <header class="absolute w-full">
    <div
      class="p-5 px-20 flex-row justify-between items-center border-b border-gray-500 text-white md:flex hidden"
    >
      <div class="flex flex-row items-center">
        <img src="../img/logo.png" alt="" class="w-14" />
        <p class="font-bold text-4xl ml-2">Sciency</p>
      </div>
      <div>
        <ul class="flex flex-row items-center">
          <button>
            <li
              class="p-2 hover:text-pink-500 hover:bg-white hover:rounded duration-300 hover:font-bold hover:border-b-2 hover:border-pink-500 uppercase"
            >
              Home
            </li>
          </button>
          <button>
            <li
              class="p-2 hover:text-pink-500 hover:bg-white hover:rounded duration-300 hover:font-bold hover:border-b-2 hover:border-pink-500 uppercase"
            >
              About
            </li>
          </button>
          <button>
            <li
              class="p-2 hover:text-pink-500 hover:bg-white hover:rounded duration-300 hover:font-bold hover:border-b-2 hover:border-pink-500 uppercase"
            >
              Team
            </li>
          </button>
          <button>
            <li
              class="p-2 hover:text-pink-500 hover:bg-white hover:rounded duration-300 hover:font-bold hover:border-b-2 hover:border-pink-500 uppercase"
            >
              Focus
            </li>
          </button>
        </ul>
      </div>
      <div>
        <button
          class="btn bg-gradient-to-tr to-purple-700 from-pink-500 btn-lg border-none text-white"
        >
          Contact
        </button>
      </div>
    </div>
    <div
      class="p-5 px-5 flex-row justify-between items-center border-b border-gray-500 text-white md:hidden flex"
    >
      <div class="flex flex-row items-center">
        <img src="../img/logo.png" alt="" class="w-14" />
        <p class="font-bold text-4xl ml-2">Sciency</p>
      </div>
      <button class="p-2" onclick="my_modal_2.showModal()"><Icon name = "mdi:menu" size = "1.8em"/></button>
    </div>
    <dialog id="my_modal_2" class="modal">
      <div class="modal-box w-11/12 h-96">
        <form method="dialog">
            <button class="btn btn-sm btn-circle btn-ghost absolute right-2 top-2">✕</button>
        </form>
        <div class="flex flex-row items-center">
            <img src="../img/logo.png" alt="" class="w-12">
            <p class="text-center ml-2 font-bold text-3xl">Sciency</p>
        </div>
        <form method="dialog" class="text-center mt-5">
            <button @click="jumpMenu(`home`)" class="w-full my-2 uppercase border-b p-1">Home</button>
            <button @click="jumpMenu(`soldout`)" class="w-full my-2 uppercase border-b p-1">Sold Out</button>
            <button @click="jumpMenu(`tickets`)" class= "w-full my-2 uppercase border-b p-1">Tickets</button>
            <button @click="jumpMenu(`speakers`)" class="w-full my-2 uppercase border-b p-1">Speakers</button>
            <button @click="jumpMenu(`organization`)" class="w-full my-2 uppercase border-b p-1">organization</button>
        </form>
      </div>
    </dialog>
  </header>
</template>

<script setup>
    const jumpMenu = (e) => {
        document.getElementById(e).scrollIntoView({behavior: 'smooth'});
    }
</script>

<style></style>
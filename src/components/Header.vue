<template>
  <header class="bg-white shadow-sm py-4">
    <div class="container flex justify-between items-center">
      <!-- logo -->
      <h1 class="font-poppins font-bold text-2xl">
        <span class="text-primary text-3xl">.eCo</span>mmerce
      </h1>
      <!-- logo end -->
      <!-- search bar -->
      <div class="relative hidden md:block">
        <MagnifyingGlassIcon
          class="size-7 text-gray-600 absolute top-2 left-2"
        />
        <input
          type="text"
          class="border-2 border-gray-200 rounded-s-md ps-10 p-2 w-[300px] outline-none"
          placeholder="Search"
        />
        <button
          class="bg-primary text-white rounded-e-md p-2 border-2 font-bold border-primary hover:bg-white hover:text-primary duration-150 w-[100px]"
        >
          Search
        </button>
      </div>
      <!-- search bar end -->
      <!-- menu -->
      <ul class="flex gap-4 items-center">
        <li class="relative">
          <ShoppingBagIcon class="size-7 text-gray-800" />
          <span
            class="bg-primary text-white rounded-full w-5 h-5 flex items-center justify-center absolute top-[-10px] right-[-10px]"
            >0</span
          >
        </li>
        <li class="relative">
          <HeartIcon class="size-7 text-gray-800" />
          <span
            class="bg-primary text-white rounded-full w-5 h-5 flex items-center justify-center absolute top-[-10px] right-[-10px]"
            >0</span
          >
        </li>
        <li>
          <UserIcon class="size-7 text-gray-800" />
        </li>
      </ul>
      <!-- menu end -->
    </div>
  </header>
  <!-- header end -->
  <!-- navbar -->
  <nav class="bg-secondary shadow-sm h-[60px] flex items-center">
    <div class="container flex justify-between items-center">
      <ul class="flex text-white">
      <li class="flex items-center bg-primary">
      <Menu />
      </li>
      <li class="hover:bg-primary p-[18px] hidden md:block">Home</li>
      <li class="hover:bg-primary p-[18px] hidden md:block">About</li>
      <li class="hover:bg-primary p-[18px] hidden md:block">Shop</li>
      <li class="hover:bg-primary p-[18px] hidden md:block">Contact</li>
    </ul>
    </div>
    <ul :class="'absolute top-0 right-0 bg-black w-[270px] h-full p-3 md:hidden duration-200 '+ open" >
      <li><XMarkIcon class="text-white size-10 cursor-pointer hover:bg-primary p-2 rounded-lg" @click="open = 'translate-x-[270px]'" /></li>
      <li class="my-6"><input type="text" placeholder="Search" class="border-2 border-secondary bg-gray-800 text-white rounded-s-md px-2 py-1 w-[160px] outline-none"><button class="bg-secondary text-white rounded-e-md p-1 border-2 font-bold border-secondary hover:bg-black duration-150 w-[80px]">search</button></li>
      <li class="text-gray-100"><span class="px-2 py-3 hover:bg-secondary w-full block ">Home</span></li>
      <li class="text-gray-100"><span class="px-2 py-3 hover:bg-secondary w-full block ">About</span></li>
      <li class="text-gray-100"><span class="px-2 py-3 hover:bg-secondary w-full block ">Shop</span></li>
      <li class="text-gray-100"><span class="px-2 py-3 hover:bg-secondary w-full block ">Contact</span></li>
    </ul>
    <button class="text-white md:hidden me-7 hover:bg-gray-800 p-2 rounded-lg" @click="open = 'translate-x-0'"><span class="text-white"><Bars3Icon class="size-7" /></span></button>
  </nav>
  <!-- navbar end -->
</template>

<script setup>
import Menu from "@/components/Menu.vue";
import { ref } from "vue";
import {
  ShoppingBagIcon,
  HeartIcon,
  UserIcon,
  MagnifyingGlassIcon,
  XMarkIcon,
  Bars3Icon,
} from "@heroicons/vue/24/outline";

const open = ref('translate-x-[270px]');

</script>

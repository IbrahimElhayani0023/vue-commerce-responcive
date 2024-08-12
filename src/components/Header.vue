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
            class="bg-primary text-white rounded-full w-5 h-5 flex items-center justify-center absolute top-[-3px] right-[-10px]"
            >0</span
          >
        </li>
        <li class="relative">
          <HeartIcon class="size-7 text-gray-800" />
          <span
            class="bg-primary text-white rounded-full w-5 h-5 flex items-center justify-center absolute top-[-3px] right-[-10px]"
            >0</span
          >
        </li>
        <li class="p-1 rounded-3xl hover:bg-gray-100">
          <UserCircleIcon class="size-8 text-gray-800" />
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
          <div class="relative inline-block text-left">
    <div class="group">
        <button type="button"
            class="inline-flex justify-center items-center w-[200px] px-4 py-2 text-sm font-medium text-white rounded-md focus:outline-none">
            Categories menu
            <!-- Dropdown arrow -->
            <svg class="w-4 h-4 ml-2 -mr-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                <path fill-rule="evenodd" d="M10 12l-5-5h10l-5 5z" />
            </svg>
        </button>

        <!-- Dropdown menu -->
        <div
            class="absolute top-8 left-0 w-[200px] mt-1 origin-top-left bg-white divide-y divide-gray-100 rounded-b-md shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transition duration-300">
            <div class="py-1">
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Phone</a>
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Tablet</a>
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Laptop</a>
            </div>
        </div>
    </div>
</div>
        </li>
        <li class="hover:bg-primary p-[18px] hidden md:block">Home</li>
        <li class="hover:bg-primary p-[18px] hidden md:block">Shop</li>
        <li class="hover:bg-primary p-[18px] hidden md:block">Contact</li>
      </ul>
    </div>
    <ul
      :class="
        'absolute top-0 right-0 bg-black w-[270px] h-full p-3 md:hidden ' +
        open
      "
    >
      <li>
        <XMarkIcon
          class="text-white size-10 cursor-pointer hover:bg-primary p-2 rounded-lg"
          @click="open = 'hidden'"
        />
      </li>
      <li class="my-6">
        <input
          type="text"
          placeholder="Search"
          class="border-2 border-secondary bg-gray-800 text-white rounded-s-md px-2 py-1 w-[160px] outline-none"
        /><button
          class="bg-secondary text-white rounded-e-md p-1 border-2 font-bold border-secondary hover:bg-black duration-150 w-[80px]"
        >
          search
        </button>
      </li>
      <li class="text-gray-100">
        <span class="px-2 py-3 hover:bg-secondary w-full block">Home</span>
      </li>
      <li class="text-gray-100">
        <span class="px-2 py-3 hover:bg-secondary w-full block">Shop</span>
      </li>
      <li class="text-gray-100">
        <span class="px-2 py-3 hover:bg-secondary w-full block">Contact</span>
      </li>
    </ul>
    <button
      class="text-white md:hidden me-7 hover:bg-gray-800 p-2 rounded-lg"
      @click="open = 'block'"
    >
      <span class="text-white"><Bars3Icon class="size-7" /></span>
    </button>
  </nav>
  <!-- navbar end -->

</template>

<script setup>
import { ref } from "vue";
import {
  ShoppingBagIcon,
  HeartIcon,
  UserCircleIcon,
  MagnifyingGlassIcon,
  XMarkIcon,
  Bars3Icon,
} from "@heroicons/vue/24/outline";

const open = ref("hidden");
</script>

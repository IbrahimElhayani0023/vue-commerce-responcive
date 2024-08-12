<template>
  <div class="container p-10 flex items-center gap-7 flex-col md:flex-row">
    <div
      class="border-2 border-primary p-3 flex justify-center rounded-lg items-center gap-3 w-2/3 md:w-1/3"
    >
      <div>
        <TruckIcon class="size-10 text-primary" />
      </div>
      <div>
        <h2 class="text-xl text-primary">Free Shipping</h2>
        <p class="text-gray-500 text-sm">Order over $150</p>
      </div>
    </div>
    <div
      class="border-2 border-primary p-3 flex justify-center rounded-lg items-center gap-3 w-2/3 md:w-1/3"
    >
      <div>
        <BanknotesIcon class="size-10 text-primary" />
      </div>
      <div>
        <h2 class="text-xl text-primary">Return Your Money</h2>
        <p class="text-gray-500 text-sm">15 days money back</p>
      </div>
    </div>
    <div
      class="border-2 border-primary p-3 flex justify-center rounded-lg items-center gap-3 w-2/3 md:w-1/3"
    >
      <div>
        <HandThumbUpIcon class="size-10 text-primary" />
      </div>
      <div>
        <h2 class="text-xl text-primary">27/7 Support</h2>
        <p class="text-gray-500 text-sm">Customer support</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import {
  TruckIcon,
  BanknotesIcon,
  HandThumbUpIcon,
} from "@heroicons/vue/24/outline";
</script>

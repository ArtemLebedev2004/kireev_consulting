<template>
  <div class="xl:w-[1280px] xl:m-auto px-3 md:px-4 xl:px-10 mt-15">
    <h2 class="text-center text-4xl">
      Наши услуги
    </h2>

    <div class="mt-7 flex flex-col gap-5">
      <div v-for="service in services" :key="service">
        <div @click="active_service(service.id)"  class="px-4 relative py-3 text-2xl border-purple border-2 rounded-xl" :class="service.active ? 'bg-liblack text-white' : ''">
          <div>
            {{ service.service }}
          </div>

          <div class="inset-y-0 absolute right-4 top-0 flex items-center">
            <img v-if="service.active" src="@/assets/icons/white_arrow.svg" alt="">
            <img v-if="!service.active" src="@/assets/icons/black_arrow.svg" alt="">
          </div>
        </div>

        <transition>
          <div v-if="service.active" class="h-[193px] mt-2 bg-ligray rounded-2xl flex justify-center items-center text-xl">
            {{ service.description }}
          </div>
        </transition>

      </div>
    </div>


  </div>

</template>

<script setup>

import { reactive } from 'vue';

let services = reactive([
  {
    id: 1,
    service: "Здесь будет услуга",
    description: "Здесь будет описание услуги",
    active: false
  },
  {
    id: 2,
    service: "Здесь будет услуга",
    description: "Здесь будет описание услуги",
    active: false
  },
  {
    id: 3,
    service: "Здесь будет услуга",
    description: "Здесь будет описание услуги",
    active: false
  },
  {
    id: 4,
    service: "Здесь будет услуга",
    description: "Здесь будет описание услуги",
    active: false
  },
  {
    id: 5,
    service: "Здесь будет услуга",
    description: "Здесь будет описание услуги",
    active: false
  },
  {
    id: 6,
    service: "Здесь будет услуга",
    description: "Здесь будет описание услуги",
    active: false
  }
])

function active_service(id) {
  if (services[id - 1].active) {
    services[id - 1].active = false
  } else {
    services[id - 1].active = true
  }
}

</script>

<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.3s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>

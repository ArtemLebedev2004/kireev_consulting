<template>
  <div class="xl:w-[1280px] xl:m-auto px-2 md:px-4 xl:px-10 ">
    <div class="lg:flex  mt-[100px] md:mt-[170px] lg:mt-40 xl:mt-50 lg:gap-10">
      <div class="lg:relative lg:basis-1/2 lg:flex lg:flex-col  lg:justify-between">
        <div>
          <h1 id="observe_h1" class=" dsfdsg
            text-[46px] md:text-[85px] lg:text-[63px] font-semibold 
            leading-12 md:leading-20 lg:leading-16
          ">
            Проекты «под ключ» для бизнеса и частных лиц
          </h1>
          
          <div class="max-lg:hidden text-[25px] mt-5">
            Гарантия 1 год
          </div>
        </div>
        

        <div @click="openModal = !openModal" class="
          max-lg:hidden
          relative
          bottom-0 
          w-full  
          text-[25px] text-white text-center
          bg-[#4F7A23] 
          rounded-4xl md:rounded-[100px]  
          mt-[18px] md:mt-[25px] xl:mt-0  
          py-5 hover:py-6 
          border-[#4F7A23]
          transition-all duration-200
          cursor-pointer
          overflow-hidden 
          before:content-['']
          before:animate-hologram
          before:block
          before:-rotate-45
          before:absolute
          before:-top-[120%]
          before:-left-[100%]
          before:w-[200%]
          before:h-[70%]
          before:bg-linear-to-b
          before:from-green-100/20
          before:bg-transparent
        ">
          Заказать звонок
        </div>
      </div>

      <div class="relative lg:flex lg:items-center mt-[20px] md:mt-[45px] lg:mt-0 lg:basis-1/2 p-3 md:p-6">
        <img src="@/assets/img/main_img.jpg" alt="" class="w-full m-auto rounded-[20px] md:rounded-[40px] lg:rounded-[24px]">
        <div class="absolute inset-0 rounded-[20px] md:rounded-[40px] lg:rounded-[30px] border-6 md:border-12 lg:border-10 border-[#4F7A23] animate-swim-border"></div>

      </div>
    </div>
    

    <div class="lg:hidden text-center mt-[18px] md:mt-[25px] text-[20px] md:text-[30px]">
      Гарантия 1 год
    </div>
    
    <div @click="openModal = !openModal" class="
      button
      overflow-hidden
      lg:hidden 
      relative z-10 
      text-[20px] md:text-[30px] text-white text-center
      bg-[#4F7A23]  
      rounded-4xl md:rounded-[100px]  
      mt-[18px] md:mt-[25px]  
      py-4 md:py-8
      before:content-['']
      before:animate-hologram
      before:block
      before:-rotate-45
      before:bg-black
      before:absolute
      before:-top-[120%]
      before:-left-[100%]
      before:w-[200%]
      before:h-[70%]
      before:bg-linear-to-b
      before:from-green-100/20
      before:bg-transparent
    ">
      Заказать звонок
    </div>
  </div>
  
  <OrderCallModal v-if="openModal" @closeModal='openModal = false'/>

</template>

<script setup>
import { ref } from 'vue';
import OrderCallModal from '../../modals/orderCallModal.vue';

document.body.scrollTop = 0

let openModal = ref(false)

</script>
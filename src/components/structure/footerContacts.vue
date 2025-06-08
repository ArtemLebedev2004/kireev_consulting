<template>
  <div class=""
  :class="idActive == 3 ? 'bg-[#4F7A23]' : 'xl:w-[1280px] xl:m-auto mt-10 xl:mt-20 xl:m-auto   px-2 md:px-4 xl:px-10 pb-2 md:pb-4 xl:pb-10'">
    <div class="
      flex flex-col 
      gap-3 md:gap-5
      bg-[#4F7A23] 
      text-white md:text-[30px] lg:text-[25px] text-center 
      py-6 md:py-10
    " 
    :class="idActive == 3 ? 'xl:w-[1280px] xl:m-auto px-2 md:px-4 xl:px-10 pb-2 md:pb-4 xl:pb-10' : 'rounded-3xl md:rounded-[45px] mt-10'">
      <div>+7-800-700-30-08</div>

      <div>blagodei30@yandex.ru</div>

      <div class="
        flex justify-center
        gap-4 md:gap-6
        mt-2 md:mt-4
      ">
        <div @click="openModal = !openModal" class="
          flex flex-col justify-center
          bg-white hover:bg-black/0
          py-[2px] px-4 md:px-8 
          text-[#4F7A23] hover:text-white font-semibold 
          rounded-full 
          border-5 border-white 
          transition-all duration-200
          cursor-pointer
        ">
          Заказать звонок
        </div>
      </div>


      <div class="
        bg-white 
        h-[2px] 
        mt-2 md:mt-4
      "></div>

      <div class="
        mt-2 
        px-6 xl:px-15 
        text-[13px] md:text-[17px]
        flex max-xl:flex-col gap-3 lg:justify-between lg:max-xl:items-center xl:items-end
      ">
        <div class="flex xl:basis-2/3 max-md:flex-col md:flex-wrap gap-3 md:gap-x-7 md:max-xl:justify-center">
          <div><router-link to="terms_of_use" class="underline">Правила пользования интернет-сайтом</router-link></div>
          <div><router-link to="terms_of_cookie" class="underline">Условия использования файлов cookie</router-link></div>
          <div><router-link to="user_agreement" class="underline">Пользовательское соглашение об обработке персональных данных</router-link></div>

        </div>
        
        <div class="mt-2 md:mt-4 xl:mt-0 text-center xl:basis-1/3 xl:text-right">© 2025</div>
      </div>
    </div>
  </div>
 

  <orderCallModal v-if="openModal" @closeModal="openModal = false" />
</template>

<script setup>
import { ref, toRefs } from 'vue';
import orderCallModal from '../modals/orderCallModal.vue';

let props = defineProps([
  'idActive'
])

let { idActive } = toRefs(props)

let openModal = ref(false)


</script>

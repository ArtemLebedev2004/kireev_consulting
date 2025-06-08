<template>
  <div class="xl:w-[1280px] xl:m-auto px-3 md:px-4 xl:px-10 mt-15">
    <div class="p-2 border-purple border-2 rounded-xl">
      <div class="h-[300px] bg-ligray rounded-xl flex justify-center items-center text-black text-3xl">
          Описание формы
      </div>
    </div>

    <h2 class="text-center text-4xl mt-15">
      Форма обратной связи
    </h2>

    <form action="" class="flex flex-col gap-[14px] mt-9 text-[20px]">
      <input type="text" placeholder="Имя" class="px-4 py-2 bg-ligray w-full rounded-[7px]">
      <input type="phone" placeholder="Телефон" class="px-4 py-2 bg-ligray w-full rounded-[7px]">
      <input type="text" placeholder="Почта" class="px-4 py-2 bg-ligray w-full rounded-[7px]">

      <div class="group mt-3 md:mt-8 text-[16px] flex gap-3 md:gap-6 xl:gap-3 items-center">
        <input id="check_circle" type="checkbox" class="hidden" required>
        
        <label for="check_circle" class="">
            <div class="w-6 h-6 md:w-8 md:h-8 xl:w-6 xl:h-6 rounded-sm border-1 xl:border-3 border-purple group-has-checked:bg-liblack"></div>
        </label>
        
        <div class="w-fit text-black leading-5 md:leading-7">Даю согласие на обработку своих персональных данных</div>
         
      </div>

      <input type="submit" value="Отправить" class="w-full py-2 md:py-4 text-center rounded-lg bg-liblack mt-3 md:mt-10 text-white">
    </form>
  </div>

</template>

<script setup>

document.body.scrollTop = 0

</script>

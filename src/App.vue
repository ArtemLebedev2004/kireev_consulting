<template>
  <router-view />

  <div id="cookie_note" class="bg-[#4F7A23] fixed z-20 text-white inset-x-0 bottom-0 lg:left-[60%] lg:right-4 lg:bottom-4 lg:rounded-[30px] px-2 md:px-4 lg:px-8 xl:px-10 py-3 lg:py-6 lg:text-[18px]" :class="openModal ? '' : 'hidden'">
    <div class="text-[20px] lg:text-[23px] font-semibold">
      Уведомление о Cookies
    </div>

      <div class="mt-2">
        Наш сайт использует файлы cookie.
        Продолжая пользоваться сайтом, вы соглашаетесь на использование нами ваших файлов cookie. <router-link to="/terms_of_cookie" class="underline font-semibold">Подробнее</router-link>
      </div>

      <div @click="openModal = !openModal" class="w-max py-2 px-4 mt-4 border-2 border-white rounded-[30px] transition-all duration-200 hover:bg-white hover:text-[#4F7A23] cursor-pointer cookie_accept ">
        Хорошо, я соглашаюсь
      </div>
  </div>
  
</template>

<style>
</style>

<script setup>
import { onMounted, ref } from 'vue';

let openModal = ref(false)

onMounted(() => {
  checkCookies();
})

function setCookie(name, value, days) {
  let expires = "";
  if (days) {
      let date = new Date();
      date.setTime(date.getTime() + (days * 24 * 60 * 60 * 1000));
      expires = "; expires=" + date.toUTCString();
  }
  document.cookie = name + "=" + (value || "") + expires + "; path=/";
}

function getCookie(name) {
  let matches = document.cookie.match(new RegExp("(?:^|; )" + name.replace(/([\.$?*|{}\(\)\[\]\\\/\+^])/g, '\\$1') + "=([^;]*)"));
  return matches ? decodeURIComponent(matches[1]) : undefined;
}

function checkCookies() {
  console.log('asdasdas')
  let cookieNote = document.getElementById('cookie_note');
  let cookieBtnAccept = cookieNote.querySelector('.cookie_accept');

  // Если куки cookies_policy нет или она просрочена, то показываем уведомление
  if (!getCookie('cookies_policy')) {
    openModal.value = true;
  }

  // При клике на кнопку устанавливаем куку cookies_policy на один год
  cookieBtnAccept.addEventListener('click', function () {
    setCookie('cookies_policy', 'true', 20);
    openModal.value = false;
  });
}

</script>
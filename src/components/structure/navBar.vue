<template>
  <nav class="
    fixed z-20
    left-0 right-0 top-0
    text-white
  " >
    <div class="px-3 py-6">
      <router-link to="#"><img src="../../assets/icons/logo.png" alt="" class="min-[420px]:w-[80%] min-[420px]:mx-auto"></router-link>
    </div>
  </nav>

</template>
<!--
<script setup>
import router from '@/router';
import { nextTick, onMounted, ref } from 'vue';

let changeBgNav = ref(false)

onMounted(() => {
  const section = router.currentRoute.value.hash.replace("#", "")

  if (section) {
    nextTick(() => window?.document?.getElementById(section)?.scrollIntoView())
  }

  observeMainNav()
})

function observeMainNav() {
  let observe_h1 = document.getElementsByTagName('h1')[0]

  let rootMarginMain = null

  if (observe_h1.offsetTop != 0) {
    rootMarginMain = '-' + (observe_h1.clientHeight + observe_h1.offsetTop - 10) + 'px 0px 0px 0px'
  } else {
    rootMarginMain = '-' + (observe_h1.clientHeight + 110) + 'px 0px 0px 0px'
  }

  let observerBgNav = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (!entry.isIntersecting) {
      changeBgNav.value = 50
      console.log(rootMarginMain)
    } else {
      changeBgNav.value = 0
    }
  });
  }, { rootMargin: rootMarginMain });

  observerBgNav.observe(observe_h1);
}
</script> -->

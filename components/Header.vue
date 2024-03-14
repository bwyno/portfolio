<template>
  <header ref="header" class="h-[80px] fixed w-full top-0 z-50">
    <div class="relative h-full">
      <div class="absolute text-white w-full m-auto h-full flex z-10">
        <div class="header-bottom w-[100%] h-full z-10">
          <div class="header-top w-[100%] scroll-watcher h-full z-10">
          </div>
        </div>
      </div>
      <nav class="absolute w-full flex justify-center items-center h-full gap-[100px] text-white z-20">
        <div class="w-[120px] flex justify-center items-center">
          <NuxtLink to="/#intro"
            class="text-[18px] hover:text-green-500 font-medium transition ease-in-out delay-150 hover:scale-110 duration-300 hover:-translate-y-1">
            Home
          </NuxtLink>
        </div>
        <div class="w-[120px] flex justify-center items-center">
          <NuxtLink to="/#tech-stack"
            class="text-[18px] hover:text-green-500 font-medium transition ease-in-out delay-150 hover:scale-110 duration-300 hover:-translate-y-1">
            Tech Stack
          </NuxtLink>
        </div>
        <div class="w-[120px] flex justify-center items-center">
          <NuxtLink to="/#projects"
            class="text-[18px] hover:text-green-500 font-medium transition ease-in-out delay-150 hover:scale-110 duration-300 hover:-translate-y-1">
            Projects
          </NuxtLink>
        </div>
      </nav>
    </div>

  </header>
</template>

<script setup>
// const header = ref()
// const scrollPosY = ref()
// onMounted(() => {
//   const handleScroll = () => {
//     scrollPosY.value = window.scrollY
//     if (scrollPosY.value > header.value.offsetTop) {
//       header.value.classList.add("header");
//     } else {
//       header.value.classList.remove("header");
//     }
//   }
//   window.addEventListener('scroll', handleScroll);
// })
</script>

<style>
.header-bottom {
  background: rgb(2, 0, 36);
  background: linear-gradient(0deg, rgba(2, 0, 36, 0) 0%, rgba(121, 78, 9, 0.5886729691876751) 35%, rgba(255, 175, 0, 0.6054796918767507) 100%);
}

.header-top {
  background: rgb(0,55,230);
background: linear-gradient(0deg, rgba(0,55,230,0.3785889355742297) 0%, rgba(29,9,121,0.6222864145658263) 50%, rgba(12,0,255,0.6615021008403361) 100%);
  mask: linear-gradient(90deg, transparent, white 20%, white 80%, transparent);
}

.scroll-watcher {
  scale: 0 1;
  opacity: 0.2;
  animation: scroll-watcher linear;
  animation-timeline: scroll();
}

@keyframes scroll-watcher {
  to {
    scale: 1 1;
    opacity: 1;
  }
}
</style>
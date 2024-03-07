<template>
  <header ref="header" class="h-[80px] fixed w-full top-0 z-50">
    <nav class="flex justify-center items-center h-full gap-[100px] text-white">
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
  </header>
</template>

<script setup>
const header = ref()
const scrollPosY = ref()
onMounted(() => {
  const handleScroll = () => {
    scrollPosY.value = window.scrollY
    if (scrollPosY.value > header.value.offsetTop) {
      header.value.classList.add("header");
    } else {
      header.value.classList.remove("header");
    }
  }
  // watchEffect(() => {
  //   if (expandMenu.value === true) {
  //     header.value.classList.remove("header");
  //   } else {
  //     header.value.classList.add("header");
  //   }  
  // })
  window.addEventListener('scroll', handleScroll);
})
</script>

<style>
header {
  transition: background-color 0.3s linear;
}

.header {
  background-color: #444343;
  border-bottom: 1px solid rgb(112, 109, 109);
}
</style>
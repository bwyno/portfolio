<template>
  <section id="intro" class="flex justify-center items-center h-screen text-white">
    <div class="grid grid-cols-2 place-items-center gap-10 px-40 mt-[80px]">
      <NuxtImg class="h-[700px] rounded-[40px] col-6" src="/bryanphoto.svg" />
      <div class="col-6 w-[80%] text-justify text-[25px]">
        Welcome to my portfolio! I'm Bryan Arnoco, a full-stack developer constantly expanding my skill set to include
        new languages and technologies. Currently skilled in <span class="text-green-500 font-bold">JavaScript</span>, <span
          class="text-green-500 font-bold">TypeScript</span>, <span class="text-green-500 font-bold">PHP</span>, <span
          class="text-green-500 font-bold">Laravel</span>, <span class="text-green-500 font-bold">Vue.js</span>, <span
          class="text-green-500 font-bold">React.js</span>, <span class="text-green-500 font-bold">React Native</span>, <span
          class="text-green-500 font-bold">Nuxt.js</span>, and <span class="text-green-500 font-bold">Node.js</span>, I'm dedicated to
        crafting immersive digital experiences. By continuously learning and integrating new languages and technologies,
        I deliver high-quality solutions that seamlessly blend robust backend systems with elegant front-end interfaces.
        Let's collaborate and build something amazing together!
      </div>
    </div>
  </section>
</template>

<style>


.image {
  -webkit-filter: grayscale(0%);
  -moz-filter: grayscale(0%);
  filter: grayscale(0%);
  transition: all 0.5s ease;
}

.image:hover {
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  filter: grayscale(100%);
}
</style>
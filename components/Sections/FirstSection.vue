<template>
  <section id="intro"
    class="absolute border-2 w-screen first-section flex justify-center items-center h-screen text-white">
    <div class="first-section-div grid grid-cols-2 place-items-center gap-10 px-40 mt-[80px]">
      <NuxtImg class="h-[700px] rounded-[40px] col-6" src="/bryanphoto.svg" />
      <div class="col-6 w-[600px] text-justify text-[25px]">
        Welcome to my portfolio! I'm Bryan Arnoco, a full-stack developer constantly expanding my skill set to include
        new languages and technologies. Currently skilled in <span class="text-green-500 font-bold">JavaScript</span>,
        <span class="text-green-500 font-bold">TypeScript</span>, <span class="text-green-500 font-bold">PHP</span>,
        <span class="text-green-500 font-bold">Laravel</span>, <span class="text-green-500 font-bold">Vue.js</span>,
        <span class="text-green-500 font-bold">React.js</span>, <span class="text-green-500 font-bold">React
          Native</span>, <span class="text-green-500 font-bold">Nuxt.js</span>, and <span
          class="text-green-500 font-bold">Node.js</span>, I'm dedicated to
        crafting immersive digital experiences. By continuously learning and integrating new languages and technologies,
        I deliver high-quality solutions that seamlessly blend robust backend systems with elegant front-end interfaces.
        Let's collaborate and build something amazing together!
      </div>
    </div>
  </section>
</template>

<style>
.first-section {
  background-color: rgba(0, 0, 0, 0.7);
  height: 10vh;
  border: 1px solid;
  width: 10vw;
  bottom: 0;
  right: 0;
  animation: increase linear forwards;
  animation-timeline: scroll(y);
  animation-range: 0 300vh;
  transform: translate(-100%, -100%) skew(-45deg);
  z-index: 10;
}

.first-section-div {
  scale: 0 0;
  animation: scale-animation linear forwards;
  animation-timeline: scroll(y);
  animation-range: 0 300vh;
}

@keyframes increase {
  0% {
    width: 10vw;
    height: 10vh;
    transform: translate(-100%, -100%) skew(-45deg);
  }

  39% {
    width: 100vw;
    height: 100vh;
    transform: translate(0, 0) skew(0deg);
    border: 1px solid;
  }
  40% {
    width: 100vw;
    height: 100vh;
    transform: translate(0, 0) skew(0deg);
    border: 0;
  }

  60% {
    width: 100vw;
    height: 100vh;
    transform: translate(0, 0) skew(0deg);
    opacity: 1;
    border: 1px solid;
  }

  90% {
    top: 0;
    left: 0;
    width: 10vw;
    height: 10vh;
    transform: translate(0, 0) skew(60deg);
    opacity: 0.1;
  }

  100% {
    opacity: 0;
  }
}

@keyframes scale-animation {
  0% {
    scale: 0 0;
  }

  40% {
    scale: 1 1;
  }

  60% {
    scale: 1 1;
  }

  90% {
    scale: 0 0;
  }

  100% {
    scale: 0 0;
  }
}
</style>
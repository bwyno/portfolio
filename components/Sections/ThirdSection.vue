<template>
  <section id="projects" class="absolute flex  justify-center third-section text-white">
    <div class="third-section-div flex flex-col gap-10 my-28">
      <div class="uppercase text-center text-[50px] text-white font-medium">Projects</div>
      <div class="grid grid-cols-3 gap-10">
        <div v-for="item in 6" class="group relative block bg-black rounded-[20px] h-[300px] w-[300px] border-2 border-slate-400 shadow-white shadow-lg" >
          <NuxtImg alt="" src="/jeepneys.jpg"
            class="absolute rounded-[20px] inset-0 h-full w-full object-cover opacity-75 transition-opacity group-hover:opacity-50" />

          <div class="relative p-4 sm:p-6 lg:p-2">
            <div>
              <div class="transform opacity-0 transition-all group-hover:translate-y-32 group-hover:opacity-100 px-2">
                <div class="text-[40px] text-green-500 font-semibold">JeepNav</div>
                <p class="text-sm text-white font-light">
                  A Mobile App for Streamlined Navigation and Fare Estimation in Cebu City
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.third-section {
  background-color: rgba(0, 0, 0, 0.7);
  height: 10vh;
  border: 1px solid;
  width: 10vw;
  bottom: 0;
  right: 0;
  animation: increase-3 linear forwards;
  animation-timeline: scroll(y);
  animation-range: 620vh;
  transform: translate(-80%, -80%) skew(-45deg);
}
.third-section-div {
  scale: 0 0;
  animation: scale-animation-3 linear forwards;
  animation-timeline: scroll(y);
  animation-range: 620vh 920vh;
}

@keyframes increase-3 {
  0% {
    width: 10vw;
    height: 10vh;
    transform: translate(-80%, -80%) skew(-45deg);
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

@keyframes scale-animation-3 {
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
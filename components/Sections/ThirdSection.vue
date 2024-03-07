<template>
  <section id="projects" class="flex py-28 justify-center third-section h-screen ">
    <div class="flex flex-col gap-10">
      <div class="uppercase text-center text-[50px] text-white font-medium">Projects</div>
      <div class="grid grid-cols-3 gap-10">
        <div v-for="item in 6" class="group relative block bg-black rounded-[20px] h-[300px] w-[300px]">
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
  background-color:rgb(32, 31, 31)c;
}
</style>
<template>
  <div class="bg h-screen w-screen">
      <SectionsFirstSection />
      <SectionsSecondSection />
      <SectionsThirdSection />
      <!-- <SectionsFourthSection /> -->
  </div>
  <Header />

  <div class="h-[1200vh]"></div>
</template>

<style>
.bg {
  position: fixed;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5),
      rgba(0, 0, 0, 0.5)), url(/bryanbackground.svg);
  ;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
}
</style>
<template>
  <div class="bg">
    <Header />
    <div class="relative">
      <SectionsFirstSection />
      <SectionsSecondSection />
      <SectionsThirdSection />
      <SectionsFourthSection />
    </div>


  </div>
</template>

<style>
.bg {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5),
      rgba(0, 0, 0, 0.5)), url(/bryanbackground.svg);
  ;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
}
</style>
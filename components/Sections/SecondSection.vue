<template>
  <section id="tech-stack" class="flex py-40 justify-center second-section h-screen text-white">
    <div class="flex flex-col gap-20 sec-inside">
      <div class="uppercase text-center text-[50px] font-medium">
        Tech Stack
      </div>
      <div class="flex flex-auto min-h-[80px] max-w-[800px] overflow-hidden scroller">
        <div class="flex space-x-4 animation text-center w-max scroller-inner">
          <div @click="getTech(tech)" v-for="tech in technologies"
            class="p-3 w-[100px] hover:border-green-500 hover:text-green-500 border-2 rounded-[20px] flex items-center justify-center  cursor-pointer">
            <NuxtImg class="w-[80%]" :src="tech.logo" ></NuxtImg>
          </div>
          <div @click="getTech(tech)" v-for="tech in technologies"
            class="p-3 w-[100px] hover:border-green-500 hover:text-green-500 border-2 rounded-[20px] flex items-center justify-center cursor-pointer">
            <NuxtImg class="w-[80%]" :src="tech.logo" ></NuxtImg>
          </div>
        </div>
      </div>
      <div class="flex flex-col gap-10 border-2 border-gray-500 h-[100%] max-w-[800px] rounded-[40px] p-5">
        <div v-if="!techItem" class="">
          Select a technology.
        </div>
        <div class="text-green-500 text-[40px]">{{ techItem ? techItem.name : "" }}</div>
        <div class="text-justify text-[14px]">
          {{ techItem ? techItem.description : "" }}
        </div>
        <div v-if="techItem">Proficiency: <span class="text-green-500">{{ techItem ? techItem.rating : "" }}</span>/5</div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const techItem = ref();
const technologies = ref([
  {
    name: "C",
    description:
      "C, my first programming language, laid the groundwork for my coding expertise. From creating basic calculators to tackling simple embedded systems, I gained a comprehensive understanding of programming essentials. Though I've shifted focus in recent projects, I'm keen to re-engage with C given the right opportunity. Its timeless versatility underscores its enduring relevance in software development.",
    rating: 3,
    logo: "/c-logo.png"
  },
  {
    name: "Java",
    description: "Java, my introduction to object-oriented programming, instilled in me the foundational principles of this paradigm. Through Java, I grasped the core tenets of OOP and developed small-scale applications. While my recent projects have not demanded Java, I remain enthusiastic about engaging with it in future endeavors that warrant its utilization.",
    rating: 2,
    logo: "/java-logo.png"
  },
  {
    name: "Python",
    description: "My interest in Python blossomed during my university studies, particularly as I delved into topics like machine learning. I'm keen to deepen my understanding of Python, especially in the context of machine learning projects. Additionally, I'm enthusiastic about exploring various Python frameworks to expand my skill set and tackle diverse challenges.",
    rating: 2,
    logo: "/python-logo.png"
  },
  {
    name: "Flutter",
    description: "Flutter was among the initial languages I explored for mobile development, though my exploration was not exhaustive. Nevertheless, I'm eager to delve deeper into the framework and work on projects that leverage its capabilities. I'm excited about the potential opportunities to further my proficiency and contribute to projects utilizing Flutter.",
    rating: 2,
    logo: "/flutter-logo.png"
  },
  {
    name: "JavaScript",
    description: "JavaScript is my programming passion, my first love. Its versatility and utility in web development have kept me enamored since the outset of my journey. I've utilized it extensively to craft dynamic, interactive websites, both in my professional work and personal projects. Its integral role in my daily endeavors only serves to deepen my admiration for its boundless potential.",
    rating: 5,
    logo: "/javascript-logo.png"
  },
  {
    name: "TypeScript",
    description: "TypeScript, a statically typed superset of JavaScript, elevates developer productivity by introducing optional static typing to the language. This feature enables developers to detect errors early in the development cycle, enhancing code maintainability and enabling better tooling support. With TypeScript, I've experienced firsthand the benefits of features like interfaces, enums, generics, and more, which have significantly streamlined my workflow. It stands as the primary language in my current projects, underscoring its indispensability in my day-to-day work.",
    rating: 4,
    logo: "/typescript-logo.png"
  },
  {
    name: "PHP",
    description: "PHP has become indispensable to me through its association with Laravel. Starting with Laravel, I've grown to appreciate PHP's versatility and power. As I continue with Laravel, I'm eager to explore other PHP frameworks to expand my skill set.",
    rating: 4,
    logo: "/php-logo.png"
  },
  {
    name: "Vue.js",
    description: "Vue.js holds a special place as my first JavaScript framework, and I've developed a deep affection for it. Its intuitive syntax, flexibility, and seamless integration with existing projects have made it a joy to work with. From its straightforward templating system to its reactive data-binding capabilities, Vue.js has empowered me to create dynamic and engaging user interfaces with ease. As I continue to harness its potential in my projects, my admiration for Vue.js only grows stronger.",
    rating: 5,
    logo: "/vue-logo.png"
  },
  {
    name: "React.js",
    description: "React.js quickly became a pivotal framework for me, crucial for my thesis project and subsequent work endeavors, including a work management system. Its component-based structure and declarative nature have streamlined UI development. As I delve deeper into React.js, its versatility and efficiency fuel my excitement to incorporate it into future projects.",
    rating: 5,
    logo: "/react-logo.png"
  },
  {
    name: "React Native",
    description: "React Native was instrumental in creating my thesis mobile application, simplifying development and accelerating my progress as a developer. Exploring its capabilities opened up a world of possibilities in mobile development. The efficiency and versatility it offers have been invaluable, inspiring me to delve deeper into mobile app development.",
    rating: 5,
    logo: "/react-native-logo.png"
  },
  {
    name: "Nuxt.js",
    description: "Nuxt.js has been my go-to Vue framework at work. Its intuitive nature and powerful features have streamlined my workflow, allowing me to build efficient and scalable applications with ease.",
    rating: 4,
    logo: "/nuxt-logo.png"
  },
  {
    name: "Node.js",
    description: "I'm currently expanding my skill set by learning Node.js, having gained proficiency in its fundamentals. I'm eager to delve deeper into Node.js frameworks, further honing my expertise and broadening my capabilities as a developer.",
    rating: 4,
    logo: "/node-logo.png"
  },
  
]);

interface Item {
  name: string;
  description: string;
  rating: number;
}

const getTech = (item: Item) => {
  techItem.value = item;
  console.log(techItem.value);
};
</script>

<style>
.second-section {
  background-color: rgba(0, 0, 0, 0.7);
  animation: fade-in linear forwards;
  animation-timeline: view();
  animation-range: entry ;
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*   */

.scroller {
  -webkit-mask: linear-gradient(90deg,
      transparent,
      white 20%,
      white 80%,
      transparent);
  mask: linear-gradient(90deg, transparent, white 20%, white 80%, transparent);
}

.scroller-inner {
  animation: slide 30s linear infinite;
}

.scroller-inner:hover {
  animation-play-state: paused;
}

@keyframes slide {
  to {
    transform: translateX(calc(-50% - 0.5rem));
  }
}
</style>

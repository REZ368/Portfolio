<template>
  <section class="py-8 px-4" id="project">
    <h2 class="text-2xl md:text-4xl font-extrabold leading-tight tracking-tight mb-6 text-center text-yellow-500">🅼🆈 🅿🆁🅾🅹🅴🅲🆃🆂</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 lg:gap-8">
      <!-- Card component repeated six times -->
      <div v-for="(project, index) in projects" :key="index" class="overflow-hidden rounded-lg shadow-lg mx-auto cursor-pointer" @mouseenter="enlargeCard($event)" @mouseleave="resetCard($event)">
        <img :src="project.image" :alt="project.title" class="w-full h-40 md:h-48 object-cover object-center">
        <div class="p-4 md:p-6 bg-teal-800">
          <h3 class="font-semibold text-lg md:text-xl mb-2 text-blue-500">{{ project.title }}</h3>
          <p class="text-gray-100 text-sm md:text-base">{{ project.description }}</p> 
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "KOPE / E-commerce",
          description: "It is an online shop specializing in selling sewing tools. Here, you can conveniently purchase a variety of sewing supplies for clothing, costumes, maps, stuffed toys, and designs about clothes.",
          image: "/images/kope.jpg",
        },
        {
          title: "JILL / E-commerce",
          description: "It is a website selling permitted products such as food, fruits, vegetables, and beverages. It has a community forum that users can inquire about products or exchange ideas on their production processes.",
          image: "/images/jill.jpg",
        },
        {
          title: "HOOD / E-commerce",
          description: "An artworks gallery website dedicated for aspiring artists selling their skills online. It helps artists showcase their new projects, including digital, graphic, illustration, 3d models, and animation arts.",
          image: "/images/hood.jpg",
        },
        {
          title: "NURR / E-commerce",
          description: "An online shop selling upper and lower clothes featuring anime prints. You can customize your favorite anime designs and styles according to your anime preferences.",
          image: "/images/nurr.jpg",
        },
        {
          title: "SUROY-TA! / ORS",
          description: "A reservation platform for tourist attractions all over Cebu City. You can create a post advertising tourist spots and reserve the attractions they offer for the tourist's.",
          image: "/images/suroyta.jpg",
        },
        {
          title: "NURR / Music App",
          description: "A music website/application where you can listen to music with zero ads. It features a chatbot that can assist you with your music preferences or rearrange the playlist for you.",
          image: "/images/csm.jpg",
        },
      ],
    };
  },
  methods: {
    enlargeCard(event) {
      event.currentTarget.style.transform = "scale(1.1)";
      event.currentTarget.style.transition = "transform 0.5s ease";
    },
    resetCard(event) {
      event.currentTarget.style.transform = "scale(1)";
    },
  },
};
</script>

<style scoped>
#project {
  background: linear-gradient(to bottom right, #453F78, #FFC94A);
}
</style>



<template>
<div id="apps" class="home flex flex-col md:flex-row items-center justify-center bg-slate-700">
    <!-- Content Section -->
    <div class="content text-center md:text-left md:mr-1 mb-10 py-12">
  <div class="intro">
    <p class="mb- text-5xl text-white pl-10 py-4 font-extrabold leading-tight tracking-tight">ＡＢＯＵＴ</p>
    <p class="text-white py-4 pl-10 pr-10 font-sans leading-tight tracking-tight line-spacing-1.5"> <!-- Added px-6 for left and right padding -->
      Greetings, I am Renz Kayle Ando, often recognized 
      as Rez across various social media platforms. 
      Originating from the Philippines, I offer a comprehensive 
      skill set as a FullStack Developer and UX/UI Designer. My
       proficiency spans technical and creative ingenuity in web development. Beyond
      this domain, I am equally passionate about digital arts and music
      engineering. Notably, my recent projects have revolved 
      around the development of E-commerce websites and online forums. 
      Fueled by an insatiable curiosity, I am dedicated to 
      remaining at the forefront of emerging technologies  and pioneering 
      coding methodologies.
    </p>
  </div>
</div>
    <!-- Image Section -->  
    <div class="image w-screen mb-1 py-1">
      <img class="w-full" src="/images/circol.png" alt="innovation">
    </div>
    <router-view></router-view>
  </div> <br><br>
</template>
<script>
export default {
  methods: {
    toggleImageAnimation() {
      const imageSection = document.getElementById('image-section');
      imageSection.classList.toggle('slide-animation');
    }
  }
};


</script>

<style scoped>
@media (min-width: 640px) {
  .h-24 {
    height: 6rem; /* Adjust the height for smaller screens */
  }
  .w-24 {
    width: 6rem; /* Adjust the width for smaller screens */
  }
}

.image {
  transition: transform 0.3s ease; /* Define the transition property */
}
.slide-animation {
  transform: translateY(-100%); /* Apply the animation */
}

#image {
  max-width: 100%; 
}
</style>

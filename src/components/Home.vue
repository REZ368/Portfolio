<template>
  <div id="apps" class="home flex flex-col md:flex-row items-center justify-center bg-slate-700">
    <!-- Content Section -->
    <div class="content text-center md:text-left md:mr-8 py-3 mb-10">
      <div class="intro">
         <br><br>
        <h1 id="typed" class="text-2x1 md:text-4x2 font-extrabold leading-tight tracking-tight mb-2 first-line: text-red-500"> </h1>
        <p class="mb-2 text-lg text-white py-4 font-extrabold leading-tight tracking-tight">ℍ𝔼𝕐, 𝕀'𝕄 𝗥𝗘𝗡𝗭 𝗞𝗔𝗬𝗟𝗘 𝗔𝗡𝗗𝗢 <br> 𝔹𝕌𝕋 𝕐𝕆𝕌 ℂ𝔸ℕ ℂ𝔸𝕃𝕃 𝕄𝔼 𝗥𝗘𝗭</p>
        <p class=" text-white py-4 font-sans leading-tight tracking-tight"> I am a full stack developer and A UX/UI designer <br>
         A BSIT student in Cordova Public College</p>
      </div>
      <div class="flex flex-wrap justify-center md:justify-start"> <!-- Button Container -->
      <router-link to="/projects" class="btn btn-primary">→ 𝘴𝘦𝘦 𝘮𝘺 𝘱𝘳𝘰𝘫𝘦𝘤𝘵𝘴</router-link>
      <router-link to="/about" class="btn btn-primary">→ 𝘮𝘰𝘳𝘦 𝘢𝘣𝘰𝘶𝘵 𝘮𝘦</router-link>
    </div>
    </div> 
    <!-- Image Section -->  
    <div class="image md:w-1/2">
      <img class="w-full" src="/images/image2.png" alt="innovation">
    </div>
    <router-view></router-view>
  </div> <br><br>
</template>
<script>
import Typed from 'typed.js'; // Importing Typed.js library

export default {
  mounted() {
    // Initialize Typed.js
    const options = {
      strings: ['WELCOME.'],
      typeSpeed: 200, // Typing speed in milliseconds
      loop: false // Loop the typing animation
    };

    const typed = new Typed('#typed', options);
  },
  methods: {
    handleGetStarted() {
      // Handle the click event of the "Get Started" button
      // Add your logic here
    }
  }
};
</script>

<style>


/* No need to define styles here since Tailwind CSS is used */
.btn {
  padding: 0.5rem 1rem;
  margin: 0.5rem;
  font-size: 1rem;
  border-radius: 0.375rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-primary {
  background-color: teal;
  color: white;
}

.btn-primary:hover {
  background-color: blue;
}

.text-4x2 {
    font-size: 4rem; /* Adjust the value as needed */
}

.md\:text-4x2 {
    font-size: 4rem; /* Adjust the value as needed */
}
</style>

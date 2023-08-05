<template>
  <div id="Project" class="lg:pt-36 max-sm:pt-64 my-auto">
    <div class="flex flex-col items-center text-white overflow-x-hidden">
      <h1 class="uppercase font-bold tracking-wider text-4xl">project</h1>
      <hr class="style1 my-4" />
      <span
        class="max-w-xl text-center text-xl leading-loose mb-20"
        data-aos="flip-up"
        data-aos-offset="200"
        data-aos-duration="1000"
        >Explore the exciting world of our projects and discover the innovative solutions we've
        crafted</span
      >
    </div>
    <div class="flex flex-col justify-around content-center flex-wrap gap-20 overflow-x-hidden">
      <div
        v-for="project in projects"
        :key="project.Id"
        :data-aos="project.aos"
        data-aos-offset="200"
        data-aos-duration="1000"
        class="flex justify-evenly items-center text-white gap-4 flex-wrap px-4"
      >
        <img :src="project.ImgSrc" :alt="project.ImgAlt" class="w-1/2" />
        <div class="flex flex-col max-w-lg max-md:items-center">
          <h1 class="text-4xl font-bold max-md:text-center">{{ project.Name }}</h1>
          <span class="my-6 max-md:text-center">{{ project.Description }}</span>
          <div class="flex gap-8">
            <a
              :href="project.Link"
              target="_blank"
              class="p-4 cursor0 border max-w-[140px] bg-w rounded-xl text-center mt-6 font-bold py-2 px-4 rounded transition duration-300 ease-in-out transform hover:-translate-y-1 hover:scale-110"
              >Live Demo<i class="fa-solid fa-share-from-square ml-2 text-white"></i
            ></a>
            <a
              :href="project.Link1"
              target="_blank"
              class="p-4 cursor0 border max-w-[140px] bg-w rounded-xl text-center mt-6 font-bold py-2 px-4 rounded transition duration-300 ease-in-out transform hover:-translate-y-1 hover:scale-110"
              >Code<i class="fa-brands ml-2 fa-github text-white"></i
            ></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { ref } from 'vue'
import Covid from '../Images/My project (4).png'
import weather from '../Images/My project (2).png'
import Todo from '../Images/My project (1).png'
import Ecommerce from '../Images/My project (3).png'
import Crypto from '../Images/crypto.png'

export default {
  setup() {
    const projects = ref([
      {
        Id: 1,
        aos: 'slide-left',
        ImgSrc: Covid,
        ImgAlt: 'Covid Center — Covid 19 tracker',
        Name: 'Covid Center — Covid 19 tracker',
        Description:
          'Developed a comprehensive COVID-19 tracker, featuring live statistics, news updates, and an interactive quick test. Utilized HTML, CSS, JavaScript, and PHP to create an engaging user interface',
        Link: 'http://covidcenter.rf.gd/index.php',
        Link1: 'https://github.com/Mohammad-Houry1/Covid-Center.git'
      },
      {
        Id: 2,
        aos: 'slide-right',
        ImgSrc: Ecommerce,
        ImgAlt: 'ShopZone — Ecommerce Website',
        Name: 'ShopZone — Ecommerce Website',
        Description:
          'Created an innovative e-commerce website with a focus on user experience and functionality. Implemented HTML, CSS, JavaScript,  Vue.js and Laravel to deliver a seamless shopping experience.',
        Link: 'https://shopzone1.netlify.app',
        Link1: 'https://github.com/Mohammad-Houry1/ShopZone-Laravel.git'
      },
      {
        Id: 3,
        aos: 'slide-left',
        ImgSrc: Crypto,
        ImgAlt: 'CryptoVerse - Crypto App',
        Name: 'CryptoVerse - Crypto App',
        Description:
          'Developed a dynamic and user-friendly crypto app, leveraging Vue.js and Tailwind CSS to deliver real-time market data, seamless trading experiences, and a modern interface supported by various APIs.',
        Link: 'https://cryptoverse12314.netlify.app',
        Link1: 'https://github.com/Mohammad-Houry1/CryptoVerse.git'
      },
      {
        Id: 4,
        aos: 'slide-right',
        ImgSrc: weather,
        ImgAlt: 'Weather Ease — Weather App',
        Name: 'Weather Ease — Weather App',
        Description:
          'Designed and developed a dynamic weather website utilizing Vue.js and Tailwind CSS, providing users with real-time weather information, intuitive interfaces, and seamless user experience.',
        Link: 'https://weather-ease.netlify.app/',
        Link1: 'https://github.com/Mohammad-Houry1/Weather-Ease-Weather-App.git'
      },
      {
        Id: 5,
        aos: 'slide-left',
        ImgSrc: Todo,
        ImgAlt: 'Todo List - App',
        Name: 'Todo List - App',
        Description:
          'The Todo List web application is a user-friendly tool that allows you to effortlessly manage and organize your tasks. With its intuitive interface, you can easily add, edit, complete, and remove tasks, ensuring you stay on top of your daily responsibilities and goals.',
        Link: 'https://todo-app-list-00.000webhostapp.com/',
        Link1: 'https://github.com/Mohammad-Houry1/Todo-TodoApp.git'
      }
    ])
    return {
      projects
    }
  }
}
</script>

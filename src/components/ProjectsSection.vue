<template>
      <div id="project" class=" bg-gradient-to-b from-black to bg-gray-800 w-full text-white h-full md:h-screen">
        <div class="max-w-screen-lg p-4 mx-auto flex flex-col justify-center w-full h-full">
              
            <div v-motion-slide-visible-left class="pb-8 duration-500">
                                    
                        <p class="text-4xl font-bold inline border-b-4 border-gray-500">Project</p>
                        <p class="py-6">Check out some of my project right here</p>
                  
            </div>
      

      <div class="relative grid sm:grid-cols-2 md:grid-cols-3 gap-8 px-12 sm:px-0">

                  <div v-for="project in projects" :key="project.id" 
                  v-motion
                  :initial="{
                        opcaity: 0,
                        x: mobile? 0: -200
                  }"
                  :visible="{
                        opacity: 1,
                        x:0
                  }"
                  :delay="project.id * 150"
                  class="duration-500 group shadow-md shadow-gray-600 rounded-lg">
         
                        <img :src="project.src" alt="" class=" rounded-md duration-200 hover:scale-105  group-hover:opacity-20">      
                        <span class="group-hover:block hidden p-1 top-32 absolute border-b-2  text-2xl font-bold text-white tracking-wider">
                              {{ project.title }}
                        </span>
                        <span class="group-hover:block hidden p-1 top-44 absolute font-bold text-gray-500">
                              {{ project.tech }}
                        </span>
                        
                        <div class="flex items-center justify-center">
                              <a :href="project.live" target="_blank" class="w-1/2 px-6 py-3 m-4 duration-200 hover: scale-105"><button>Demo</button></a>
                              <a :href="project.code" target="_blank" class="w-1/2 px-6 py-3 m-4 duration-200 hover: scale-105"><button>Code</button></a>
                              
                              
                        </div>
                  </div>


                  
            
      </div>
        </div>
      </div>
</template>
<script>

import project from '../assets/project.png'
import project2 from '../assets/project2.png'
import project3 from '../assets/project3.png'
export default {
    setup() {

      const mobile = window.innerWidth<=768 ? true : false
      const projects = [
            {
                  id: 1,
                  src: project,
                  title: 'My Portfolio',
                  tech: 'VueJS, Tailwind CSS',
                  code: 'https://github.com/jmatthewa/portfolio',
                  live: 'https://jamesmatthew.pages.dev/'

            },
            {
                  id: 2,
                  src: project2,
                  code: 'https://github.com/jmatthewa/the-strawhat-fit',
                  live: 'https://strawhatfit.pages.dev/',
                  title: 'The Strawhat Fit',
                  tech: 'VueJS, CSS, Javascript'
            },
            {
                  id: 3,
                  src: project3
            }
      ]

      return { projects,mobile }
    },
}
</script>

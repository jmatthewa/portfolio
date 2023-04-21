<template>
      <div id="project" class=" bg-gradient-to-b from-black to bg-gray-800 w-full text-white h-full md:h-screen">
        <div class="max-w-screen-lg p-4 mx-auto flex flex-col justify-center w-full h-full">
            <transition name="slide" appear>
            
                  <div class="pb-8">
                                          
                              <p class="text-4xl font-bold inline border-b-4 border-gray-500">Project</p>
                              <p class="py-6">Check out some of my project right here</p>
                     
                  </div>
            </transition>

            <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-8 px-12 sm:px-0">

                
                  
                        <div  v-for="project in projects" :key="project.id" class="shadow-md shadow-gray-600 rounded-lg">
                            <transition name="slide2" appear>
                            
                                  <img :src="project.src" alt="" class="rounded-md duration-200 hover:scale-105 hover:opacity-20">
                                  
                              </transition>
                              <span class="text-2xl font-bold text-white tracking-wider">
                                    {{ project.title }}
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

export default {
    setup() {

      const projects = [
            {
                  id: 1,
                  src: project,
                  title: 'Vue JS project'
            },
            {
                  id: 2,
                  src: project2,
                  code: 'https://github.com/jmatthewa/the-strawhat-fit',
                  live: 'https://strawhatfit.pages.dev/'
            },
            {
                  id: 3,
                  src: project
            }
      ]

      return { projects }
    }
}
</script>

<style>
      .slide-enter-active,
      .slide-leave-active {
      transition: opacity 5s ease;
      }

      .slide-enter-from,
      .slide-leave-to {
      opacity: 0;
      }


      .slide2-enter-active {
      transition: all 5s ease-in-out;
      }

      .slide2-enter-from{
      transform: translateX(50px);
      opacity: 0;
      }
</style>
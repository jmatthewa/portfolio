<template>
      <div name="project" class="bg-gradient-to-b from-black to bg-gray-800 w-full text-white md:h-screen">
        <div class="max-w-screen-lg p-4 mx-auto flex flex-col justify-center w-full h-full">
            <div class="pb-8">
                  <p class="text-4xl font-bold inline border-b-4 border-gray-500">Project</p>
                  <p class="py-6">Check out some of my project right here</p>
            </div>

            <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-8 px-12 sm:px-0">

                  <div  v-for="project in projects" :key="project.id" class="shadow-md shadow-gray-600 rounded-lg">
                        <img :src="project.src" alt="" class="rounded-md duration-200 hover:scale-105">

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
                  src: project
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

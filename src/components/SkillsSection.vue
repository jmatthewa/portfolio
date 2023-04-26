<template>
    <div id="skills" class="bg-gradient-to-b from-gray-800 to-black w-full h-full md:h-screen">
        <div class="max-w-screen-lg mx-auto p-4 flex flex-col justify-center w-full h-full text-white">
            <div v-motion-slide-visible-left class="duration-500">
                <p class=" text-4xl font-bold border-b-4 border-gray-500 p-2 inline">Skills</p>
                <p class="py-6">These are the technologies I've worked with</p>
            </div>

            <div class="w-full grid grid-cols-2 sm:grid-cols-3 gap-8 text-center py-8 sm:px-0">
                <div  v-for="skill in skills" :key="skill.id" :class="skill.style" 
                  
                v-motion
                  :initial="{
                        scale: 0,
    
                  }"
                  :visible="{
                        scale: 1,
                    
                  }"
                  :delay="skill.id * 150"
                class="shadow-md  duration-500 py-2 rounded-lg"
       >
                    <img :src="skill.src" class="w-20 mx-auto hover:scale-150 duration-700">
                    <p class="mt-4">{{ skill.title }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

import css from '../assets/css.png'
import github from '../assets/github.png'
import html from '../assets/html.png'
import javascript from '../assets/javascript.png'
import mongo from '../assets/mongo.png'
import node from '../assets/node.png'
import reactI from '../assets/react.png'
import tailwind from '../assets/tailwind.png'
import vue from '../assets/vue.png'

export default {
    setup() {
        
        const skills = [
            {
                id:4,
                src: css,
                title: 'CSS',
                style: 'shadow-blue-500'
            },
            {
                id:5,
                src: github,
                title: 'Github',
                style: 'shadow-gray-500'
            },
            {
                id:6,
                src: html,
                title: 'HTML',
                style: 'shadow-orange-500'
            },
            {
                id:7,
                src: javascript,
                title: 'JavaScript',
                style: 'shadow-yellow-500'
            },
            {
                id:8,
                src: mongo,
                title: 'MongoDB',
                style: 'shadow-green-500'
            },
            {
                id:9,
                src: node,
                title: 'Node',
                style: 'shadow-green-500'
            },
            {
                id:10,
                src: reactI,
                title: 'React',
                style: 'shadow-blue-500'
            },
            {
                id:11,
                src: tailwind,
                title: 'Tailwind',
                style: 'shadow-sky-500'
            },
            {
                id:12,
                src: vue,
                title: 'Vue',
                style: 'shadow-green-500'
            }
        ]

        return {
            skills
        }
    }
}
</script>

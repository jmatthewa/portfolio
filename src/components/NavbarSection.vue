<template>
    <!-- <fa icon="bars"/> -->
    <div class="flex justify-between items-center w-full h-20 text-white px-4 bg-black fixed">

        <div>
            <h1 class="text-5xl font-signature ml-2">Matt</h1>
        </div>

        <ul class="hidden md:flex">
            <li v-for="link in links" :key="link.id" class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200">{{ link.link }}</li>
        </ul>

        <div @click="showDropDown" class="cursor-pointer pr-4 z-10 text-gray-500 md:hidden">
           <fa v-if="nav" icon="times" size="2x"/>
           <fa v-else icon="bars" size="2x"/>
        </div>

        <ul v-show="nav" class="flex flex-col justify-center items-center absolute top-0 left-0 w-full h-screen bg-gradient-to-b from-black to-gray-800 text-gray-500">
            <li v-for="link in links" :key="link.id" class="px-4 cursor-pointer capitalize py-6 text-4xl">{{ link.link }}</li>
           
        </ul>
    </div>
</template>
<script>
import { ref } from 'vue';


export default {
    setup() {

        const nav = ref(false)

        const links = [
            {
                id: 1,
                link: 'home'
            },
            {
                id: 2,
                link: 'about'
            },
            {
                id: 3,
                link: 'projects'
            },
            {
                id: 4,
                link: 'skills'
            },
            {
                id: 5,
                link: 'contact'
            }
     ]

     const showDropDown = function() {
        return this.nav = !this.nav
     }

     return {
        links,showDropDown,nav
     }
    }
}
</script>
<style>
    
</style>
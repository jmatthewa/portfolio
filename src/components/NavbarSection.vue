<template>
    <!-- <fa icon="bars"/> -->
    <div class="z-10 top-0 flex justify-between items-center w-full h-20 text-white px-4 bg-black fixed">

        <div>
            <h1 class=" text-5xl font-signature ml-2">Matt</h1>
        </div>

        <ul class="hidden md:flex">
            <li class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200" @click="scroll2('hero')">Home</li>
            <li class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200" @click="scroll2('about')">About</li>
            <li class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200" @click="scroll2('project')">Project</li>
            <li class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200" @click="scroll2('skills')">Skills</li>
            <li class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200" @click="scroll2('contact')">Contact</li>
        </ul>

        <div @click="showDropDown" class="cursor-pointer pr-4 z-10 text-gray-500 md:hidden">
           <fa v-if="nav" icon="times"  size="2x"/>
           <fa v-else icon="bars"  size="2x"/>
        </div>

        <ul v-show="nav" class="flex flex-col justify-center items-center absolute top-0 left-0 w-full h-screen bg-gradient-to-b from-black to-gray-800 text-gray-500">
            <li class="px-4 cursor-pointer capitalize py-6 text-4xl" @click="scroll('hero')">Home</li>
            <li class="px-4 cursor-pointer capitalize py-6 text-4xl" @click="scroll('about')">About</li>
            <li class="px-4 cursor-pointer capitalize py-6 text-4xl" @click="scroll('project')">Project</li>
            <li class="px-4 cursor-pointer capitalize py-6 text-4xl" @click="scroll('skills')">Skills</li>
            <li class="px-4 cursor-pointer capitalize py-6 text-4xl" @click="scroll('contact')">Contact</li>
           
        </ul>
    </div>
</template>
<script>
import { ref } from 'vue';


export default {
    setup() {

    const nav = ref(false)  

    const showDropDown = function() {
        return this.nav = !this.nav
     }

    function scroll(id) {
            this.nav = !this.nav
            const element = document.getElementById(id);
            element.scrollIntoView({ behavior: 'smooth' });
    }
    function scroll2(id) {
       
       const element = document.getElementById(id);
       element.scrollIntoView({ behavior: 'smooth' });
    }
    
     return {
        showDropDown,nav,scroll, scroll2
     }
    }
}
</script>
<style>
    
</style>
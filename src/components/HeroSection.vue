<template>
    <div name="hero" class="h-screen w-full bg-gradient-to-b from-black via-black to-gray-800">
        <div class="max-w-screen-lg mx-auto flex flex-col items-center justify-center h-full px-4 sm:flex-row">
            <div class="flex flex-col justify-center h-full">
                <h2 class="text-4xl sm:text-7xl font-bold text-white">
                    I'm a Full Stack Developer
                </h2>
                <p class="text-gray-500 py-4 max-w-md">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis itaque quae molestiae, laboriosam dolorem perferendis inventore ut perspiciatis reiciendis vol
                    uptates voluptatum earum sed natus? Consequuntur deleniti nisi animi esse a!
                </p>
                
                <div>
                    <button class="group text-white w-fit px-6 py-3 my-2 items-center rounded-md bg-gradient-to-r from-cyan-500 to-blue-500">
                        Portfolio 
               
                        <fa :icon="['fas', 'angles-right']" class="group-hover:rotate-90 duration-300 ml-1"/>
                       
                    </button>
                </div>
            </div>
            <div>
                <img :src="HeroImage" alt="" class="mx-auto w-2/3 sm:w-full">
            </div>
        </div>
    </div>
</template>
<script>


import HeroImage from '../assets/heroImage.png'



export default {
    setup() {



        return {
            HeroImage
        }
    }
}
</script>
<style>
    
</style>
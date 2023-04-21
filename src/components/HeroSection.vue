<template>
    <div id="hero"  class=" h-96 sm:h-screen w-full bg-gradient-to-b from-black via-black to-gray-800">
        <div class="mt-20 max-w-screen-lg mx-auto flex flex-col items-center justify-center h-full px-4 sm:flex-row sm:mt-0">
            <div class="flex flex-col justify-center h-full">
                <transition name="slide" appear>
                    <h2  class=" text-4xl  sm:text-7xl  font-bold text-white">
                        I'm a Full Stack Developer
                    </h2>
                
                </transition>
                <transition name="slide2" appear>
                
                    <p class="text-gray-500 py-4 max-w-md">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis itaque quae molestiae, laboriosam dolorem perferendis inventore ut perspiciatis reiciendis vol
                        uptates voluptatum earum sed natus? Consequuntur deleniti nisi animi esse a!
                    </p>
                    
                </transition>
                <transition name="slide" appear>
                
                    <div>
                        <button @click="scroll('project')" class="group text-white w-fit px-6 py-3 my-2 items-center rounded-md bg-gradient-to-r from-cyan-500 to-blue-500">
                            Portfolio 
                   
                            <fa :icon="['fas', 'angles-right']" class="group-hover:rotate-90 duration-300 ml-1"/>
                           
                        </button>
                    </div>
                </transition>
            </div>
            <transition name="slide" appear>
            
                <div>
                    <img :src="HeroImage" alt="" class="hidden md:block mx-auto w-2/3 sm:w-full">
                </div>
            </transition>
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
    },
    methods: {
        scroll(id) {
        
            const element = document.getElementById(id);
            element.scrollIntoView({ behavior: 'smooth' });
    }
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
  transition: all 2s ease-out;
}



.slide2-enter-from{
  transform: translateX(100px);
  opacity: 0;
}
</style>
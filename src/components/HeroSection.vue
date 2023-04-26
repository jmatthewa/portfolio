<template>
    <div id="hero"  class=" h-96 sm:h-screen w-full bg-gradient-to-b from-black via-black to-gray-800">
        <div class="mt-20 max-w-screen-lg mx-auto flex flex-col items-center justify-center h-full px-4 sm:flex-row sm:mt-0">
            <div  class="flex flex-col justify-center h-full">
             
                    <h2 v-motion-fade
                    class="duration-500 text-4xl  sm:text-7xl  font-bold text-white">
                        I'm a
                   </h2>
    
                

                <h3 class="pt-2">
                    <span class="typed-text text-white"> {{ typingText }}</span>
                <span   class="cursor inline ml-1 w-1">&nbsp;</span>
             
                </h3>
                
         
                
                    <p  v-motion-fade class="duration-500 text-gray-500 py-4 max-w-md">
                        Hello and welcome! My name is James Matthew, and I am a web developer building user-friendly, responsive, and visually appealing websites and web applications
                    </p>
                    
      
                    <div>
                        <button  v-motion-fade @click="scroll('project')" class="group text-white w-fit px-6 py-3 my-2 items-center rounded-md bg-gradient-to-r from-cyan-500 to-blue-500">
                            Portfolio 
                   
                            <fa :icon="['fas', 'angles-right']" class="group-hover:rotate-90 duration-300 ml-1"/>
                           
                        </button>
                    </div>
         
            </div>

            
                <div>
                    <img  v-motion-fade :src="HeroImage" alt="" class="duration-500 hidden md:block mx-auto w-2/3 sm:w-full">
                </div>
      
        </div>
    </div>
</template>
<script>



import { computed, ref, onMounted } from 'vue';
import HeroImage from '../assets/heroImage.png'



export default {
    
    setup() {

        const words = ref(['Front-end Developer','Back-end Developer','Full-stack Developer']);
        const currentIndex = ref(0);
        const currentWord = computed(() => words.value[currentIndex.value]);
        const currentLetterIndex = ref(0);

        const typingText = computed(() => {
        return currentWord.value.substring(0, currentLetterIndex.value);
        });

        const startTyping = () => {
        setInterval(() => {
            if (currentLetterIndex.value < currentWord.value.length) {
            currentLetterIndex.value++;
            } else {
            currentLetterIndex.value = 0;
            currentIndex.value++;
            if (currentIndex.value >= words.value.length) {
                currentIndex.value = 0;
            }
            }
        }, 100)


    }
    function scroll(id){
            const element = document.getElementById(id);
            element.scrollIntoView({ behavior: 'smooth'})

        }


    onMounted(() => {
      startTyping();
    });

        return {
            HeroImage,
            typingText,
            scroll

        }
    }
        
    
}
</script>
<style>



span.cursor {
    background-color: #fff;
    animation: cursorBlink 1s infinite;
   
}

@keyframes cursorBlink {
    49% { background-color: #fff;}
    50% { background-color: transparent;}
    99% { background-color: transparent;}
}
</style>
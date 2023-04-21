<template>
    <div id="about" class="w-full h-full bg-gradient-to-b from-gray-800 to-black text-white
        ">

        <div class="max-w-screen-lg  mx-auto flex flex-col p-4 justify-center items-center  w-full h-full md:flex-row ">
            <transition name="slide2" appear>
            
                <div class="flex flex-col justify-center h-full gap-5">
                    <img :src="heroImage" alt="" class="-scale-x-100  mx-auto w-2/3 md:w-full mix-blend-lighten animate-pulse">
                   
                </div>
            </transition>
            <div>

            <transition name="slide" appear>
            
                <p class="text-3xl font-bold inline border-b-4 border-gray-500">About</p>
            </transition>
            <transition name="slide3" appear>
            
                <p class="text-lg mt-10">
                    Hello and welcome! My name is James Matthew, and I am a web developer building user-friendly, responsive, and visually appealing websites and web applications.
                </p> 
            </transition>
                <br><br>
            <transition name="slide4" appear>
                <p class="text-lg">
                I specialize in developing websites using a combination of front-end and back-end technologies, including HTML, CSS, JavaScript, React, Vue, Node.js,MongoDB, and SQL. I am also familiar with various web development tools, such as Git,and VS Code.
            </p>
        </transition>
            <br><br>

            <transition name="slide5" appear>
            <p class="text-lg">

                My passion for web development stems from my love for problem-solving and creativity. I enjoy finding innovative solutions to complex problems.
                <br><br>
            </p>
        </transition>

            <transition name="slide6" appear>
            <p class="text-lg">
                In my portfolio, you will find examples of my personal projects, including websites and web applications that I have designed and developed. I am always looking for new and exciting projects to work on, so if you have any web development needs, please feel free to reach out to me!
    

            </p>
        </transition>
            </div>
        </div>
    



    </div>
</template>
<script>
import heroImage from '../assets/heroImage.png'
export default {
    setup() {
        

        return {
            heroImage
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

.slide3-enter-active {
  transition: all 2s ease-out;
  transition-delay: .5s;
}

.slide3-enter-from{
  transform: translateX(-100px);
  opacity: 0;
}
.slide4-enter-active {
  transition: all 2s ease-out;
  transition-delay: 1.5s;
}

.slide4-enter-from{
  transform: translateX(-100px);
  opacity: 0;
}

.slide5-enter-active {
  transition: all 2s ease-out;
  transition-delay: 2.5s;
}

.slide5-enter-from{
  transform: translateX(-100px);
  opacity: 0;
}
.slide6-enter-active {
  transition: all 2s ease-out;
  transition-delay: 3.5s;
}

.slide6-enter-from{
  transform: translateX(-100px);
  opacity: 0;
}



</style>
<template>
    <div id="about" class="w-full h-full bg-gradient-to-b from-gray-800 to-black text-white md:h-screen">

        <div class="max-w-screen-lg  mx-auto flex flex-col p-4 justify-center items-center  w-full h-full md:flex-row ">
       
            
                <div v-motion-pop-visible class="duration-500 flex flex-col justify-center h-full gap-5">
                    <img :src="heroImage" alt="" class="-scale-x-100  mx-auto w-2/3 md:w-full mix-blend-lighten animate-pulse">
                   
                </div>
 
            <div>
              <div v-motion
              :initial="{
                opacity: 0,
                x: -100
              }"
              :visible="{
                opacity: 1,
                x: 0
              }"
              class="duration-500"
              >
                <p class=" text-3xl font-bold inline border-b-4 border-gray-500">About</p>

              </div>

            <div v-motion
              :initial="{
                opacity: 0,
                x: -100
              }"
              :visible="{
                opacity: 1,
                x: 0
              }"
              :delay="100"
              class="duration-500"
              >
              
              <p class="text-lg mt-10">
                  Hello and welcome! My name is James Matthew, and I am a web developer building user-friendly, responsive, and visually appealing websites and web applications.
              </p> 
            </div>
    
                <br><br>
          <div v-motion
              :initial="{
                opacity: 0,
                x: -100
              }"
              :visible="{
                opacity: 1,
                x: 0
              }"
              :delay="250"
              class="duration-500"
             >
                <p class="text-lg">
                I specialize in developing websites using a combination of front-end and back-end technologies, including HTML, CSS, JavaScript, React, Vue, Node.js,MongoDB, and SQL. I am also familiar with various web development tools, such as Git,and VS Code.
               </p>
            
          </div>

            <br><br>

       <div v-motion
              :initial="{
                opacity: 0,
                x: -100
              }"
              :visible="{
                opacity: 1,
                x: 0
              }"
              :delay="450"
              class="duration-500"
             >
         <p class="text-lg">

             My passion for web development stems from my love for problem-solving and creativity. I enjoy finding innovative solutions to complex problems.
             <br><br>
         </p>

       </div>
        <div v-motion
              :initial="{
                opacity: 0,
                x: -100
              }"
              :visible="{
                opacity: 1,
                x: 0
              }"
              :delay="600"
              class="duration-500"
             >
          <p class="text-lg">
              In my portfolio, you will find examples of my personal projects, including websites and web applications that I have designed and developed. I am always looking for new and exciting projects to work on, so if you have any web development needs, please feel free to reach out to me!
  

          </p>

        </div>

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

<template>
    <div id="contact" class="w-full h-full md:h-screen bg-gradient-to-b from-black to-gray-800 p-4 text-white">
        <div class="flex flex-col p-4 justify-center max-w-screen-lg mx-auto h-full">
            <div v-motion-slide-visible-left class="pb-8 duration-500">
              
                    <p class="text-4xl font-bold inline border-b-4 border-gray-500">Contact</p>
                    <p class="py-6">Submit the form below to get in touch with me</p>
                </div>

                <div class="flex justify-center items-center">
                    <form div v-motion-pop-visible action="https://getform.io/f/d206e430-3b23-43ea-8d30-dde954b86255" method="POST" class="flex flex-col w-full md:w-1/2">
                        <input  type="text" name="name" placeholder="Enter your name" class="duration-500 p-2 bg-transparent border-2 rounded-md text-white focus:outline-none">
                        <input  type="text" name="email" placeholder="Enter your email" class="duration-500 my-4 p-2 bg-transparent border-2 rounded-md text-white focus:outline-none">
                    
                        <textarea   name="message" placeholder="Enter your message" rows="10" class="duration-500 p-2 bg-transparent border-2 rounded-md text-white focus:outline-none"></textarea>
                    <button   class="text-white bg-gradient-to-b from-cyan-500 to-blue-500 px-6 py-3 my-8 mx-auto flex item-center rounded-md hover:scale-110 duration-300">Let's talk</button>
                    </form>
                </div>
            </div>
        
    </div>
</template>
<script>
export default {
    
}
</script>

<template>
    <div class="p-5 h-34 flex flex-col items-center justify-center text-white bg-gradient-to-b from-gray-800 to-black">
        <div class="flex flex-col ">
            <h1 class="flex text-5xl p-5 font-signature items-center justify-center">Matt</h1>

            <div class="flex items-center justify-between">
                <a href="https://www.linkedin.com/in/james-matthew-atanacio-0b0882173/"  target="_blank"> <fa :icon="['fab','linkedin']" size="xl"/></a>
                <a href="https://github.com/jmatthewa"   target="_blank"><fa :icon="['fab','github']" size="xl"/></a>
                <a href="mailto:matthew_1147@yahoo.com"  target="_blank"><fa :icon="['fas','envelope']" size="xl"/></a>
            </div>


          
        </div>
        <p class="flex items-center justify-center p-10 text-xs">created by: James Matthew &copy; {{ new Date().getFullYear() }}</p>
    </div>
</template>
<script>
export default {
    setup() {

        // const date = new Date();

        // return {

        //     date
        // }
    }


}
</script>

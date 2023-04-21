<template>
    <div class="hidden lg:flex flex-col top-[35%] left-0 fixed">
        <ul>
            <li class="flex justify-between items-center w-40 h-14 px-4 bg-gray-500 ml-[-100px] hover:ml-[-10px] hover:rounded-md duration-300 first:rounded-tr-md last:rounded-br-md">
                <a href="https://www.linkedin.com/in/james-matthew-atanacio-0b0882173/" class="flex justify-between items-center w-full text-white" target="_blank">
                    Linkedin <fa :icon="['fab','linkedin']" size="xl"/>
                </a>

            </li>
            <li class="flex justify-between items-center w-40 h-14 px-4 bg-gray-500 ml-[-100px] hover:ml-[-10px] hover:rounded-md duration-300 first:rounded-tr-md last:rounded-br-md">
                <a href="https://github.com/jmatthewa" class="flex justify-between items-center w-full text-white"  target="_blank">
                    Github <fa :icon="['fab','github']" size="xl"/>
                </a>
            </li>

            <li class="flex justify-between items-center w-40 h-14 px-4 bg-gray-500 ml-[-100px] hover:ml-[-10px] hover:rounded-md duration-300 first:rounded-tr-md last:rounded-br-md">
                <a href="mailto:matthew_1147@yahoo.com" class="flex justify-between items-center w-full text-white"  target="_blank">
                    Mail <fa :icon="['fas','envelope']" size="xl"/>
                </a>
          </li>

                <li class="flex justify-between items-center w-40 h-14 px-4 bg-gray-500 ml-[-100px] hover:ml-[-10px] hover:rounded-md duration-300 first:rounded-tr-md last:rounded-br-md">
                    <a href="../assets/cv.pdf" class="flex justify-between items-center w-full text-white" download target="_blank">
                    Resume <fa :icon="['fas','id-card']" size="xl"/>
                </a>
              </li>

        </ul>
    </div>
</template>
<script>



export default {



    setup() {
        
        const links = [
            {
                id: 1,
                name: 'Linkedin',
                myIcon : ['fab','linkedin'],
                href: 'https://www.linkedin.com/in/james-matthew-atanacio-0b0882173/',
             
            },
            {
                id: 2,
                name: 'Github',
                myIcon : ['fab','github'],
                href: 'https://github.com/jmatthewa'
            },
            {
                id: 3,
                name: 'Mail',
                myIcon : ['fas','envelope'],
                href: 'mailto:matthew_1147@yahoo.com'
            }
            ,{
                id: 4,
                name: 'Resume',
                myIcon : ['fas','id-card'],
                href: '/cv.pdf'
                
            }
        ]

        return {
            links
        }
    }    
}
</script>
<style>
    
</style>
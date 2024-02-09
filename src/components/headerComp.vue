<script>
export default {
    name:'headerComp',
    data(){
        return{
            navLinks:[
                 {info:'CHARACTERS', href:'#personaggi'},
                 {info:'COMICS', href:'#personaggi'},
                 {info:'MOVIES', href:'#personaggi'},
                 {info:'TV', href:'#personaggi'},
                 {info:'GAMES', href:'#personaggi'},
                 {info:'COLLECTIBLES', href:'#personaggi'},
                 {info:'VIDEOS', href:'#personaggi'},
                 {info:'FANS', href:'#personaggi'},
                 {info:'NEWS', href:'#personaggi'},
                 {info:'SHOP', href:'#personaggi'},
            ]
        }
    }
}
</script>

<template>
    
  <nav class="container mx-auto flex justify-between items-center py-4 px-6">
    <div class="flex items-center">
        <img src="../assets/img/dc-logo.png" alt="DC Logo" class="h-8 mr-6">
    </div>
    <ul class="flex">
          <li class="mr-6"
           v-for="link in navLinks" :key="link.text">
            <a :href="link.href" class="hover:text-gray-300" >{{ link.info }}</a>
          </li>
    </ul>      
  </nav>


</template>

<style scoped>



</style>

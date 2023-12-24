<template>
  <v-app-bar app color="black" dark falt class="px-12">
    <v-btn>
        <!-- fas fa-camera - Bu da bir tür ikon kamera ikonu -->
    <v-icon color="purple" left class="nr-2">fas fa-signature</v-icon>
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-purple">Home</v-btn>
    <v-btn text @click="scroll('about')" class="text-purple">About</v-btn>
    <v-btn text @click="scroll('portfolio')" class="text-purple">Portfolio</v-btn>
    <v-btn text @click="scroll('page')" class="text-purple">Blog</v-btn>

  </v-app-bar>
</template>

<script>
export default {
 methods:{
    scroll(refname){
        const element = document.getElementById(refname);
        element.scrollInotView({behavior:'smooth'});
    }
 }
}
</script>
 
 
<template>
    <div>
      <v-toolbar
        image="https://static.vecteezy.com/system/resources/previews/017/560/766/non_2x/banner-pattern-of-white-sneakers-isolated-on-viva-magenta-background-sportive-pair-of-shoes-for-mockup-fashionable-stylish-sports-casual-shoes-modern-and-minimalist-wallpaper-photo.jpg"
        dark
        height="150"
      >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
  
        <v-toolbar-title  
        ><h1 style="color: orange">Collector Shoe's</h1></v-toolbar-title>
  
        <v-spacer></v-spacer>
  
        <carrito class="mr-5"
         :productos="productos"
        >

        </carrito>
      </v-toolbar>
      
    </div>
  </template>
  <script>
  export default {
    props:{
      productos : Array,
    }
  }
  </script>
  <style scoped>
   
  </style>
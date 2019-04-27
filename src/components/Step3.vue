<template>
  <v-layout my-4 row justify-space-start wrap> 
    <v-flex md-12>
      <v-card class="pa-5 text-md-center">
        <h4 class="headline">Your score is</h4>
        <h2 class="teal--text py-4 display-4" >720</h2>
        <p class="subheading">The score has been shared with the Lending Company.</p>
      </v-card>
    </v-flex>
    
 
  </v-layout>

</template>

<script>

  export default {
    props: {
      groups: Array
    },
    data() {
      return {
  
 
      }
        
    },
    mounted() {
      
    }
 
  }
</script>
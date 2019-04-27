<template>
  <v-layout my-4 row justify-space-start wrap> 

    <template v-for="(group) in groups">
      
        <v-chip
          v-for="(item, index) in group.items.filter(item => item.authorized)"
          :key="index"
          outline
        >
        {{item.title}}
        </v-chip>
      
    </template>

 
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
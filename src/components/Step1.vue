<template>
  <v-layout md12 my-4 row justify-space-start wrap>
    <v-flex md6 d-flex v-for="group in groups" :key="group.type" pa-2 >
      <v-card>
        <v-list subheader> 
          <v-subheader>{{group.type}}</v-subheader>     
          
            <v-list-tile
              v-for="item in group.items"
              :key="item.title"
              avatar
              class="my-2"
            >
            
            <v-img
              :src="item.logo"
              height="40px"
              max-width="100px"
              contain
              />

              <v-list-tile-content class="px-4">
                <v-list-tile-title v-html="item.title"></v-list-tile-title>
              </v-list-tile-content>

              <v-list-tile-action>
                <v-btn v-if="!item.authorized" color="info" > Authorize </v-btn>
                <v-icon v-else color="success" large>check</v-icon>
              </v-list-tile-action>

              
            </v-list-tile>
        </v-list>
        
  
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
        
    }
 
  }
</script>
<template>
  <v-container >
     
  <v-card class="mx-auto"  width="800">
    <v-card-actions> 
  <v-text-field
        v-model="search"
        prepend-icon="mdi-magnify"
        label="Search by email address,phone number or user UID"
        single-line
        hide-details
      ></v-text-field>
      <div class="pt-4">
        <v-btn disabled>
        add user
      </v-btn>
       <v-icon link>mdi-reload</v-icon>
        <v-icon link>mdi-wrench</v-icon>
      </div>
      
    </v-card-actions>
    
   
    <v-data-table
      :headers="headers"
     :items="empty"
      search=""
    ></v-data-table>
  </v-card>
  </v-container>
 
</template>
<script>
  export default {

    data: () => ({
      headers:[
       { text:'Identifier', value:'identifier'},
       { text:'Provider', value:'provider'},
       {text:'Created',value:'created'},
       {text:'Signed in',value:'signed in'},
       {text:'User UID',value:'user UID'}
        ]
    }),
  }
</script>

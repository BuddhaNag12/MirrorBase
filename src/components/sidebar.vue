<template>
  <v-card class="overflow-hidden">

    <v-app-bar
     
      color="#F5F7F9"
      app
    flat
    height="100"
    prominent

    >

      <v-app-bar-nav-icon class=" hidden-md-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
  
     <v-toolbar-title > Authentication</v-toolbar-title>

      <v-spacer></v-spacer>
       <div class="pa-2">
             <v-btn text>
        Go to docs
      </v-btn>
      <v-btn icon >
        <v-icon >mdi-bell</v-icon>
      </v-btn>
       <v-avatar>
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    
       </div>
       

      <template v-slot:extension>
        <v-tabs align-with-title >
          <v-tab>Users</v-tab>
          <v-tab>Sign-in methods</v-tab>
          <v-tab>Templates</v-tab>
          <v-tab>Usages</v-tab>
        </v-tabs>
      </template>
        
    </v-app-bar>
     <v-navigation-drawer
      v-model="drawer"
         app
       dark
       color=" #43c6ac"
       :mini-variant="mini"
      
    >
    <v-list color="#2A313D">
     
        <v-list-item class="px-0">
        <v-list-item-content class="pa-2">
         <v-list-item-title :class="mini && 'text--hide' " class="pa-2">
            Mirrorbase
         </v-list-item-title>
         <v-list-item :class="mini && 'pa-0 iconleft'">
     <v-icon  @click="mini=!mini" v-if="mini" text>mdi-menu-right</v-icon>
      <v-icon  @click="mini=!mini" v-else text>mdi-menu-left</v-icon>
    </v-list-item>
        </v-list-item-content>

      </v-list-item>
      <v-divider > </v-divider>
      <v-list-item class="px-0">
           <v-icon class="pa-2">mdi-home</v-icon>
              <v-list-item-title color="#B1A088" :class="mini && 'text--hide'">
                  
            Project overview
          </v-list-item-title>
          <v-divider
      class="mx-2"
      inset
      vertical
    ></v-divider>
    <v-icon>mdi-account-circle</v-icon>
      </v-list-item>
    </v-list>
           <v-divider > </v-divider>
    <v-list color="#2A313D">
               <v-list-item-title class="pl-2 " :class="mini && 'text--hide'"> 
                Develop
           </v-list-item-title>
        <v-list-item-content color="grey">
         <v-list-item link class="px-0">
             <v-icon class="pa-2">mdi-account-multiple</v-icon>
             Authentication
       </v-list-item>
         <v-list-item link class="px-0">
                  <v-icon class="pa-2">mdi-server</v-icon>
             Database
       </v-list-item>
         <v-list-item link class="px-0">
                  <v-icon class="pa-2">mdi-folder</v-icon>
             Storage
       </v-list-item>
            <v-list-item link class="px-0">
                  <v-icon class="pa-2">mdi-earth</v-icon>
             Hosting
       </v-list-item >
           <v-list-item link class="px-0">
                 <v-icon class="pa-2">mdi-loupe</v-icon>
             Functions
       </v-list-item>
           <v-list-item link class="px-0">
                 <v-icon class="pa-2">mdi-forklift</v-icon>
             ML Kit
       </v-list-item>
        </v-list-item-content>
    </v-list>
    <v-divider></v-divider>
    <v-list color="#2A313D"  class="pa-1" >
        <v-list-item-title  class="pl-2" :class="mini && 'text--hide'">Quality</v-list-item-title>
           <v-list-item-content  >
            <v-list-item  link class="px-0">
                   <v-icon class="pa-2">mdi-google-analytics</v-icon> Analytics
            </v-list-item  >
             <v-list-item  link class="px-0">
                   <v-icon class="pa-2">mdi-speedometer</v-icon> Perfomance
            </v-list-item>
             <v-list-item  link class="px-0"> 
                   <v-icon class="pa-2">mdi-comment-check</v-icon> Test Lab
            </v-list-item>
           </v-list-item-content>
    </v-list>
    
    </v-navigation-drawer>
  </v-card>
</template>

<script>
export default {
    data:()=>({
        drawer:true,
        mini:false,
        
    }),


}
</script>


<style scoped>
.text--hide{
    display: none;
}

</style>
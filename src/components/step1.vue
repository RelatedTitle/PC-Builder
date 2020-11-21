<template>
<div>
   <v-card
    elevation="8"
    color="secondary"
   >
       <v-card-title>Usage</v-card-title>
       <v-container>
    <v-row> 
        <template v-for="(usagetype, i) in usagetypes">
            <v-col
             :key="i"
            >
                <v-hover v-slot="{ hover }">
                    <v-card
                     class="usagetype rounded-lg"
                     :elevation="hover ? 12 : 2"
                     :class="{ 'on-hover': hover }"
                     width="200"
                     height="200"
                    >   
                    <v-container>
                        <v-icon> {{ usagetype.icon }} </v-icon> 
                        <span class="text-h6"> {{ usagetype.title }} </span>
                        <v-divider></v-divider>
                        <span> {{ usagetype.subtitle }}</span>
                    </v-container>
                    </v-card>
                </v-hover>
            </v-col>
        </template>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
    </v-row>
       </v-container>
   <v-divider></v-divider>
   <v-card-title>Features</v-card-title>
    <v-container>
     <v-checkbox
      :label="`RGB Lighting`"
     >
     </v-checkbox>
    </v-container>
   </v-card>
</div>
</template>

<script>
  export default {
    name: 'step1',
    data: () => ({
        usagetypes: [
            {
                title: "Gaming",
                subtitle: "",
                icon: ""
            },
            {
                title: "Streaming",
                subtitle: "Live-streaming",
                icon: "fa-trophy" 
            },
            {
                title: "Photo/Video Editing",
                subtitle: "Live-streaming",
                icon: "fa-trophy" 
            },
            {
                title: "Photo/Video Editing",
                subtitle: "Live-streaming",
                icon: "fa-trophy" 
            },
        ]
    }),
  }
</script>

<style scoped>

.usagetype {

  transition: opacity .25s ease-in-out;
}

.usagetype:not(.on-hover) {
  opacity: 0.75;
 }

</style>
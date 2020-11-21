<template>
  <v-container>
    <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step
        :complete="e1 > 1"
        step="1"
      >
        Step 1
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step
        :complete="e1 > 2"
        step="2"
      >
        Name of step 2
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="3">
        Name of step 3
      </v-stepper-step>
    </v-stepper-header>

    <v-stepper-items>
      <v-stepper-content step="1">
        <v-container>
          <Step1/>
        </v-container>
        <v-btn
          color="primary"
          @click="e1 = 2"
        >
          Continue
        </v-btn>
      </v-stepper-content>

      <v-stepper-content step="2">
        <v-card
          class="mb-12"
          color="grey lighten-1"
          height="200px"
        ></v-card>

        <v-btn
          color="primary"
          @click="e1 = 3"
        >
          Continue
        </v-btn>

        <v-btn
        @click="e1 = 1" 
        text
        >
          Back
        </v-btn>
      </v-stepper-content>

      <v-stepper-content step="3">
        <v-card
          class="mb-12"
          color="grey lighten-1"
          height="200px"
        ></v-card>

        <v-btn
          color="primary"
          to="/about"
        >
          Continue
        </v-btn>

        <v-btn 
        text
        @click="e1 = 2"
        >
          Back
        </v-btn>
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
  </v-container>
</template>



<script>
import Step1 from '@/components/step1.vue'


  export default {
    name: 'builder',
     data () {
      return {
        e1: 1,
      }
    },
    components: {
      Step1
    }
  }
</script>

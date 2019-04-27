<template>
  <div>
    <v-container  grid-list-md style="margin-bottom: 5em;">
      <Steps :step="step"/>
      <Step1 v-if="step === 1" :groups="groups" />
      <Step2 v-if="step === 2" :groups="groups"/>
      <Step3 v-if="step === 3" />
    </v-container>
    <v-footer fixed class="pa-5">
      <v-btn color="warning" @click="step--" v-if="step > 1 ">
        Back
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn color="error" @click="step++" v-if="step < 3">
        {{ step === 2 ? "Confirm" : "Continue" }}
      </v-btn>
    </v-footer>
  </div>
</template>

<script>
  import Steps from '../components/Steps'
  import Step1 from '../components/Step1'
  import Step2 from '../components/Step2'
  import Step3 from '../components/Step3'

  export default {
    components: {
      Steps,
      Step1,
      Step2,
      Step3
    },
    data() {
      return {
        step: 1,
        groups: [
        {
          type: "Identification",
          items: [
            {
              title: "uPort",
              logo:  "uport_logo.png",
              authorized: true
            },
            {
              title: "Bloom",
              logo:  "bloom_logo.png",
              authorized: false
            }
           ],
        },
        {
          type: "Finance",
          items: [
            {
              title: "N26",
              logo:  "n26_logo.png",
              authorized: true
            },
            {
              title: "Bank Of America",
              logo:  "bank_of_america_logo.png",
              authorized: false
            },
            {
              title: "Paypal",
              logo:  "paypal_logo.png",
              authorized: false
            }
           ],
        },
        {
          type: "Professional",
          items: [
            {
              title: "Github",
              logo:  "github_logo.png",
              authorized: true
            },
            {
              title: "GitCoin",
              logo:  "gitcoin_logo.png",
              authorized: true
            },
            {
              title: "Linkedin",
              logo:  "linkedin_logo.png",
              authorized: false
            },
           ]
        },
        {
          type: "Reputation",
          items: [
            {
              title: "Amazon",
              logo:  "amazon_logo.png",
              authorized: true
            },
            {
              title: "Uber",
              logo:  "uber_logo.png",
              authorized: false
            },
            {
              title: "Instacart",
              logo:  "instacart_logo.png",
              authorized: false
            },
           ]
        },
        {
          type: "Medical",
          items: [
            {
              title: "Health",
              logo:  "apple_health_logo.png",
              authorized: true
            },
            {
              title: "Nike Running",
              logo:  "nike_running_logo.png",
              authorized: true
            }
           ]
        }

      ],
      }
    },

  }
</script>

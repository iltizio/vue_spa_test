<template>
  <v-app>
    <v-content class="indigo lighten-2">
      <section>
          <v-layout
            column
            wrap
            class="my-4"
            align-center
          >
            <v-flex xs12>
              <v-container grid-list-xm>
                <v-layout row wrap align-center>
                  <v-flex xs12 md6>
                    <v-card class="elevation-0 transparent">
                      <v-card-text class="text-xs-center">
                        <v-icon x-large class="amber--text text--lighten-1">face</v-icon>
                      </v-card-text>
                      <v-card-title primary-title class="layout justify-center">
                        <div class="headline text-xs-center">About</div>
                      </v-card-title>
                      <v-card-text>
                        Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. 
                        Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. 
                        Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti. 
                      </v-card-text>
                    </v-card>
                  </v-flex>
                  <v-flex xs12 md6>
                    <v-card class="elevation-0 transparent">
                      <v-card-text class="text-xs-center">
                        <v-icon x-large class="yellow--text text--darken-3">rate_review</v-icon>
                      </v-card-text>
                      <v-card-title primary-title class="layout justify-center">
                        <div class="headline text-xs-center">Review</div>
                      </v-card-title>
                      <v-card-text>
                        Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. 
                        Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. 
                        Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti. 
                      </v-card-text>
                    </v-card>
                  </v-flex>
                </v-layout>
              </v-container>
            </v-flex>
          </v-layout>
      </section>
    </v-content>
  </v-app>
</template>

<script>
  export default {
    name: 'Home',
    data () {
      return {
        //msg: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
      }
    }
  }
</script>
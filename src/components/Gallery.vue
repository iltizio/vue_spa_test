<!--template>
  <v-carousel delimiter-icon="stop">
    <v-carousel-item v-for="(item,i) in items" v-bind:src="item.src" :key="i"></v-carousel-item>
  </v-carousel>
</template-->
<template>
  <v-content>
    <v-container fluid fill-height>
      <v-carousel delimiter-icon="fingerprint" interval="600000">
        <v-carousel-item v-for="(item,i) in items" :key="i">
            <v-layout>
                <v-flex xs12 sm6 offset-sm3>
                    <v-card>
                        <v-container fluid class="purple lighten-4">
                            <v-card-media v-bind:src="item.src" height="200px" contain @click.native.stop="imageDialog(item.src)">
                            </v-card-media>
                        </v-container>
                        <v-card-title primary-title>
                        <div>
                            <h3 class="headline mb-0">{{item.title}}</h3>
                            <div>{{item.description}}</div>
                        </div>
                        </v-card-title>
                        <v-card-actions>
                        <v-btn flat color="orange" @click.native.stop="imageDialog(item.src)">View</v-btn>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-carousel-item>
        <v-dialog v-model="dialog" max-width="600">
          <v-card>
            <v-card-media v-bind:src="dialogImg" height="400px" width="600px" contain></v-card-media>
          </v-card>
        </v-dialog>
      </v-carousel>
    </v-container>
  </v-content>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Title",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          src: "https://picsum.photos/300/200?image=1082"
        },
        {
          title: "Title",
          description: "Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. \
                        Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. \
                        Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.",
          src: "https://picsum.photos/600/800?image=1033"
        },
        {
          title: "Title",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          src: "https://picsum.photos/500/?image=1076"
        },
        {
          title: "Title",
          description: "Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. \
                        Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. \
                        Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.",
          src: "https://picsum.photos/800/600?image=1060"
        }
      ],
      dialog: false,
      dialogImg: ""
    };
  },
  methods: {
    imageDialog: function(imgSrc) {
      this.dialog = true;
      this.dialogImg = imgSrc;
    }
  }
};
</script>

<style>
.carousel__left .btn,
.carousel__right .btn {
  color: rgb(170, 20, 20) !important;
}
.carousel__controls {
  background: purple;
}
.carousel__controls__item {
  color: yellow !important;
}
</style>
<template>
  <v-app>
  <v-container>
    <v-layout row wrap>
      <v-flex md12>
        <v-carousel>
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>
        </v-carousel>
      </v-flex>
<v-flex>
<h4>Promoções da Semana</h4>
<v-row dense>
        <v-col
          v-for="card in products"
          :key="card.title"
          :cols="card.flex"
        >
          <v-card>
            <v-img
              :src="card.src"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title v-text="card.title"></v-card-title>
            </v-img>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn icon>
                <v-icon>mdi-heart</v-icon>
              </v-btn>

              <v-btn icon>
                <v-icon>mdi-bookmark</v-icon>
              </v-btn>

              <v-btn icon>
                <v-icon>mdi-share-variant</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      </v-flex>
      <v-flex md12 >
        
        
        
      </v-flex>
    </v-layout>
     </v-container>
  </v-app>



</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg"
        }
      ],

      products: [
        {
          title: 'Pre-fab homes', src: require("@/static/images/product1.png"), flex: 3,
          productTitle: "ABCN",
          
          productId: 1
        },
        {
          title: 'Favorite road trips', src: require("@/static/images/product2.png"), flex: 3,
          productTitle: "KARMA",
         
          productId: 2
        },
        {
          title: 'Best airlines', src: require("@/static/images/product3.png"), flex: 3,
          productTitle: "Tino",
          
          productId: 3
        },
        {
          title: 'Best airlines', src: require("@/static/images/product4.png"), flex: 3,
          productTitle: "EFG",
          productId: 4
        }
      ]
    };
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

<template>
  <v-container fluid>
    <v-divider></v-divider>

    <v-row class="my-15">
      <v-col cols="4">
        <v-card>
          <v-card-text>
            <v-list v-model:opened="opened">
              <v-list-group value="categories">
                <template v-slot:activator="{ props }">
                  <v-list-item
                    title="Categories"
                    v-bind="props"
                    class="bg-primary pa-4"
                  ></v-list-item>
                </template>
                <v-list>
                  <v-list-item
                    v-for="(category, i) in categories"
                    :key="i"
                    link
                    >{{ category }}</v-list-item
                  >
                </v-list>
              </v-list-group>
            </v-list>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col>
        <div class="d-flex">
          <v-btn
            variant="text"
            color="primary"
            class="text-capitalize text-subtitle-1"
            >Home</v-btn
          >
          <v-btn variant="text" class="text-capitalize text-subtitle-1"
            >Shop</v-btn
          >
          <v-btn variant="text" class="text-capitalize text-subtitle-1"
            >Shop Detail</v-btn
          >
          <v-menu open-on-hover close-delay="3000">
            <template v-slot:activator="{ props }">
              <v-btn
                variant="text"
                class="text-capitalize text-subtitle-1"
                v-bind="props"
                >Pages</v-btn
              >
            </template>
            <v-card rounded="0">
              <v-card-text class="d-flex flex-column">
                <v-btn variant="text" color="primary" class="text-capitalize"
                  >Shopping Cart</v-btn
                >
                <v-btn variant="text" class="text-capitalize">Checkout</v-btn>
              </v-card-text>
            </v-card>
          </v-menu>
          <v-btn variant="text" class="text-capitalize text-subtitle-1"
            >Contact</v-btn
          >
          <v-spacer></v-spacer>
          <v-btn variant="text" class="text-capitalize text-subtitle-1"
            >Login</v-btn
          >
          <v-btn variant="text" class="text-capitalize text-subtitle-1"
            >Register</v-btn
          >
        </div>
        <v-carousel class="mt-4" hide-delimiters continuous cycle>
          <v-carousel-item
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
            cover
            gradient="to bottom, rgba(0,0,0,0.3), rgba(0,0,0,0.7)"
            content-class="align-center justify-center d-flex"
          >
            <div class="">
              <p
                class="text-h4 font-weight-light text-center text-uppercase text-white"
              >
                10% off your first order
              </p>
              <p
                class="font-weight-bold text-center text-white mt-3"
                style="font-size: 70px"
              >
                Fashionable dress
              </p>
              <div class="d-flex justify-center mt-5">
                <v-btn class="mt-4" rounded="0">Shop Now</v-btn>
              </div>
            </div>
          </v-carousel-item>
          <v-carousel-item
            src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
            gradient="to bottom, rgba(0,0,0,0.3), rgba(0,0,0,0.7)"
            cover
            content-class="align-center justify-center d-flex"
          >
            <div class="">
              <p
                class="text-h4 font-weight-light text-center text-uppercase text-white"
              >
                10% off your first order
              </p>
              <p
                class="font-weight-bold text-center text-white mt-3"
                style="font-size: 70px"
              >
                Fashionable dress
              </p>
              <div class="d-flex justify-center mt-5">
                <v-btn class="mt-4" rounded="0">Shop Now</v-btn>
              </div>
            </div></v-carousel-item
          >
        </v-carousel>
      </v-col>
    </v-row>
    <v-row class="mt-15">
      <v-col>
        <v-card class="pa-8" elevation="0">
          <div class="d-flex">
            <v-icon color="primary" size="30">mdi-check</v-icon>
            <p class="font-weight-bold text-h6 ml-5">Quality Product</p>
          </div>
        </v-card>
      </v-col>
      <v-col>
        <v-card class="pa-8" elevation="0">
          <div class="d-flex">
            <v-icon color="primary" size="30">mdi-truck-fast</v-icon>
            <p class="font-weight-bold text-h6 ml-5">Free Shipping</p>
          </div>
        </v-card>
      </v-col>
      <v-col>
        <v-card class="pa-8" elevation="0">
          <div class="d-flex">
            <v-icon color="primary" size="30">mdi-swap-horizontal</v-icon>
            <p class="font-weight-bold text-h6 ml-5">14-Day Return</p>
          </div>
        </v-card>
      </v-col>
      <v-col>
        <v-card class="pa-8" elevation="0">
          <div class="d-flex">
            <v-icon color="primary" size="30">mdi-phone-in-talk</v-icon>
            <p class="font-weight-bold text-h6 ml-5">24/7 Support</p>
          </div>
        </v-card>
      </v-col>
    </v-row>

    <v-row class="my-15">
      <v-col v-for="sexyme in 6" cols="4">
        <v-card>
          <v-card-text>
            <!-- <div class="d-flex justify-end"><p>15 Products</p></div> -->
            <p class="d-flex justify-end">15 Products</p>
            <v-img
              height="300"
              src="https://themewagon.github.io/eshopper/img/cat-1.jpg"
            ></v-img>
            <p class="font-weight-bold text-h5 mt-5">Men's Dresses</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row class="mt-15">
      <v-col>
        <v-card color="secondary">
          <v-card-text>
            <v-row>
              <v-col>
                <v-img
                  height="300"
                  src="https://themewagon.github.io/eshopper/img/offer-1.png"
                ></v-img>
              </v-col>
              <v-col>
                <p class="text-end my-5 text-primary">20% OFF THE ALL ORDER</p>
                <P class="text-end my-5 text-h3 font-weight-bold"
                  >Spring Collection</P
                >
                <div class="d-flex justify-end my-5">
                  <v-btn variant="outlined" color="primary">Shop now</v-btn>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col>
        <v-card color="#edf1ff">
          <v-card-text>
            <v-row>
              <v-col>
                <v-img
                  height="300"
                  src="https://themewagon.github.io/eshopper/img/offer-2.png"
                ></v-img>
              </v-col>
              <v-col>
                <p class="text-end my-5 text-primary">20% OFF THE ALL ORDER</p>
                <P class="text-end my-5 text-h3 font-weight-bold"
                  >Spring Collection</P
                >
                <div class="d-flex justify-end my-5">
                  <v-btn variant="outlined" color="primary">Shop now</v-btn>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="12" class="my-15">
        <p class="text-h3 text-center mt-5 font-weight-bold font-">
          Trandy Products
        </p>
      </v-col>
    </v-row>

    <v-row>
      <v-card v-for="pic in 8" class="mx-3 my-5">
        <v-img
          src="https://themewagon.github.io/eshopper/img/product-5.jpg"
        ></v-img>
        <v-card-subtitle class="pt-4"> Colorful Stylish shirt </v-card-subtitle>
        <v-card-text> $123 <span class="n"> $123</span> </v-card-text>
        <v-card-actions>
          <v-btn>
            <v-icon color="primary" size="30">mdi-eye-outline</v-icon>
            View Detail</v-btn
          >
          <v-btn>
            <v-icon color="primary" size="30">mdi-cart</v-icon>
            View Detail</v-btn
          >
        </v-card-actions>
      </v-card>
    </v-row>

    <v-row>
      <v-col cols="12" class="mt-15">
        <v-card color="secondary" class="mt-10">
          <v-card-text class="text-center">
            <p class="text-h3 font-weight-bold">Stay updated</p>
            <p class="mt-10">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae,
              impedit. Culpa, commodi nesciunt totam esse saepe adipisci?
              Pariatur, ipsa, expedita aut et maxime cumque quod deserunt quas
              cum error, ipsam quae saepe magni. Porro, magni perferendis
              voluptates tempore eaque maiores.
            </p>
            <v-text-field
              class="mt-10 mb-15"
              variant="solo"
              density="comfortable"
              append-inner-icon="mdi-magnify"
              label="Email goes here"
            ></v-text-field>
          </v-card-text> </v-card
      ></v-col>
    </v-row>

    <v-row class="my-15">
      <v-col cols="12">
        <p class="text-h3 text-center mt-5 font-weight-bold font-">
          Just Arrived
        </p>
      </v-col>
    </v-row>

    <v-row>
      <v-card v-for="pic in 8" class="mx-3 my-5">
        <v-img
          src="https://themewagon.github.io/eshopper/img/product-5.jpg"
        ></v-img>
        <v-card-subtitle class="pt-4"> Colorful Stylish shirt </v-card-subtitle>
        <v-card-text> $123 <span class="n"> $123</span> </v-card-text>
        <v-card-actions>
          <v-btn>
            <v-icon color="primary" size="30">mdi-eye-outline</v-icon>
            View Detail</v-btn
          >
          <v-btn>
            <v-icon color="primary" size="30">mdi-cart</v-icon>
            View Detail</v-btn
          >
        </v-card-actions>
      </v-card>
    </v-row>

    <v-row class="mx-5 my-13">
      <v-card v-for="tag in 6" cols="4" width="170px" class="mx-5 my-10">
        <v-img src="https://themewagon.github.io/eshopper/img/vendor-1.jpg">
        </v-img>
      </v-card>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from "vue";

const opened = ref(["categories"]);
const categories = [
  "Shirts",
  "Jeans",
  "Swimwear",
  "Sleepwear",
  "Sportswear",
  "Jumpsuits",
  "Blazers",
  "Jackets",
  "Shoes",
];
</script>

<style>
.custom-ul {
  list-style-type: none; /* Remove default bullets */
}

.custom-ul li::before {
  content: ">"; /* Use ">" as the bullet */
  margin-right: 5px; /* Adjust spacing between bullet and content */
  color: black;
  /* Add any additional styles you want for the bullet here */
}

.custom-ul li {
  margin: 10px 0; /* Adjust the spacing between list items */
}
.custom-ul li:hover {
  text-decoration: underline;
}

.n {
  text-decoration: line-through;
}
</style>

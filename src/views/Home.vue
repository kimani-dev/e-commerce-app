<template>
  <v-container fluid>
    <v-divider></v-divider>
    <v-row>
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

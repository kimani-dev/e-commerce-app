<template>
  <v-container fluid>
    <v-row class="bg-secondary" dense>
      <v-col class="px-0 ma-0">
        <v-btn variant="text" class="text-capitalize">FAQs</v-btn>
        <span>|</span>
        <v-btn variant="text" class="text-capitalize">Help</v-btn>
        <span>|</span>
        <v-btn variant="text" class="text-capitalize">Support</v-btn>
      </v-col>
      <v-col class="d-flex justify-end">
        <v-btn icon="mdi-facebook" variant="flat"></v-btn>
        <v-btn icon="mdi-twitter" variant="flat"> </v-btn>
        <v-btn icon="mdi-youtube" variant="flat"> </v-btn>
        <v-btn icon="mdi-instagram" variant="flat"> </v-btn>
        <v-btn icon="mdi-linkedin" variant="flat"> </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div class="d-flex">
          <v-card width="60px" elevation="0.2">
            <p class="text-h3 font-weight-bold text-primary text-center pa-2">
              E
            </p>
          </v-card>
          <p class="text-h3 font-weight-bold my-auto ml-3">Shopper</p>
        </div>
      </v-col>
      <v-col>
        <v-text-field
          variant="solo"
          density="comfortable"
          append-inner-icon="mdi-magnify"
          label="Search for products"
        ></v-text-field>
      </v-col>
      <v-col class="d-flex justify-end">
        <v-card height="50px" rounded="0">
          <div>
            <v-card-text class="d-flex">
              <v-icon class="my-auto" color="primary">mdi-heart</v-icon>
              <p class="ml-2 text-subtitle-1">0</p>
            </v-card-text>
          </div>
        </v-card>
        <v-card height="50px" class="ml-3" rounded="0">
          <div>
            <v-card-text class="d-flex">
              <v-icon class="my-auto" color="primary">mdi-cart</v-icon>
              <p class="ml-2 text-subtitle-1">0</p>
            </v-card-text>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

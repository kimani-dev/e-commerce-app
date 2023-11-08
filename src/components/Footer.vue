<template>
  <div>
    <v-row class="my-15">
      <v-col cols="4">
        <div class="d-flex">
          <v-card width="60px" elevation="0.2" color="white">
            <p class="text-h3 font-weight-bold text-primary text-center pa-2">
              E
            </p>
          </v-card>
          <p class="text-h3 font-weight-bold my-auto ml-3">Shopper</p>
        </div>

        <p class="mt-5">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores,
          velit! Autem necessitatibus suscipit aperiam aut obcaecati eius ad
          cumque ab.
        </p>
        <p class="mt-7">
          <v-icon color="primary">mdi-google-maps</v-icon>
          123 Street, Nairobi, Kenya
        </p>
        <p class="mt-5">
          <v-icon color="primary">mdi-email-box</v-icon>
          info@example.com
        </p>
        <p class="mt-5">
          <v-icon color="primary">mdi-phone</v-icon>
          +2547777111111
        </p>
      </v-col>

      <v-col>
        <p class="text-h4 mt-4 mb-9 font-weight-bold">Quick Links</p>
        <ul class="custom-ul">
          <li>Home</li>
          <li>Our Shop</li>
          <li>Shop Detail</li>
          <li>Shopping Cart</li>
          <li>Checkout</li>
          <li>Contact Us</li>
        </ul>
      </v-col>

      <v-col>
        <p class="text-h4 mt-4 mb-9 font-weight-bold">Quick Links</p>
        <ul class="custom-ul">
          <li>Home</li>
          <li>Our Shop</li>
          <li>Shop Detail</li>
          <li>Shopping Cart</li>
          <li>Checkout</li>
          <li>Contact Us</li>
        </ul>
      </v-col>

      <v-col>
        <p class="text-h4 mt-4 mb-9 font-weight-bold">News Letter</p>
        <v-textarea label="Your name" solo background-color="white" rows="1">
        </v-textarea>
        <v-textarea
          label="Your name"
          solo
          background-color="gray lighten-2"
          rows="1"
        >
        </v-textarea>
        <v-btn color="primary" class="p-10" style="width: 350px; height: 60px">
          <span class="text-h5 font-weight-light" style="color: black"
            >Subscribe Now !
          </span>
        </v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<script setup></script>
<style scoped>
div {
  background-color: #edf1ff;
}
</style>

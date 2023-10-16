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
                  <v-list-item title="Categories" v-bind="props" class="bg-primary pa-4"></v-list-item>
                </template>
                <v-list>
                  <v-list-item v-for="(category, i) in categories" :key="i" link>{{
                    category
                  }}</v-list-item>
                </v-list>
              </v-list-group>
            </v-list>
          </v-card-text>
        </v-card>
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

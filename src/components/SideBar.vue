<template>
  <v-navigation-drawer expand-on-hover rail>
    <v-list>
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
        subtitle="bennylu1105@gmailcom"
        title="Benjamin Lupa"
      ></v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item
        prepend-icon="mdi-image"
        title="Color Gallery"
        value="color"
        @click="selectOption(true)"
      />
      <v-list-item
        prepend-icon="mdi-dialpad"
        title="Grey Gallery"
        value="color"
        @click="selectOption(false)"
      />
    </v-list>
  </v-navigation-drawer>
</template>
<script setup>
import { defineEmits } from "vue";

const emits = defineEmits(["selectOption"]);

const selectOption = (isColor) => {
  emits("selectOption", isColor);
};
</script>

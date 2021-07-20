<template>
  <v-container> <Title></Title> </v-container>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "../components/HelloWorld.vue";
import Title from "../components/Title.vue";

export default defineComponent({
  name: "Home",

  components: {
    Title,
  },
});
</script>

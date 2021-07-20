<template>
  <v-app-bar app flat class="appbar" dense>
    <v-app-bar-title class="pr-1 pl-1">
      <v-avatar>
        <img :src="require(`../assets/logo.png`)" alt="" />
      </v-avatar>
    </v-app-bar-title>
    <v-app-bar-title class="text-subtitle-1 pl-0"> 電気野菜 </v-app-bar-title>

    <v-divider inset vertical></v-divider>

    <div class="pl-4 links">
      <v-btn
        v-for="(item, index) in links"
        :key="index"
        text
        class="text-subtitle-1"
        @click="$router.push(item.link)"
      >
        {{ item.name }}
      </v-btn>
    </div>
  </v-app-bar>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    title: String,
    logo_path: String,
  },
  data() {
    return {
      links: [
        { name: "ホーム", link: "/" },
        { name: "ヘルプ", link: "/help" },
      ],
    };
  },
});
</script>


<style scoped>
.appbar {
  border-bottom: 1px solid rgba(0, 0, 0, 0.12);
}
</style>
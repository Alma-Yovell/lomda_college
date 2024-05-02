<template>
  <div id="app">
    <div>
        <open-screen v-if="this.page === 0"  @next-page='nextPage'> </open-screen>
        <home-page v-if="this.page === 1"></home-page>
    </div>
  </div>
</template>
 
<script>
import openScreen from "@/components/openScreen.vue";
import homePage from "@/components/homePage.vue";

export default {
  name: "app",
  components: {
    openScreen,
    homePage
  },
  data() {
    return {
      page: 0,
    };
  },
  methods: {
    nextPage() {
      this.page++;
    },
  },
};
</script>

<style>
@font-face {
  font-family: Karantina;
  src: url("assets/fonts/Karantina-Regular.ttf");
}

@font-face {
  font-family: Assistant;
  src: url("assets/fonts/Assistant-VariableFont_wght.ttf");
}

body,
html {
  margin: 0;
  padding: 0;
  height: 100%;
  overflow: hidden;
  direction: rtl;
}

</style>
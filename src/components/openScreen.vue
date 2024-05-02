<template>
  <div id="open-screen">
    <div class="shadow"></div>
    <img :src="require('@/assets/imgs/gifCollege.gif')" alt="logoGif" id="logoGif" />
    <img :src="require('@/assets/imgs/collegeLogo.png')" alt="logo" id="logo" />
    <div id="open-text">
      <div class="titles" id="open-div1">
        ברוכים הבאים למכללה הלאומית לאיתנות ישראלית של פיקוד העורף!
      </div>
      <div class="titles" id="open-div2">
        בלומדה זו תלמדו קצת על עשייתינו בשגרה ובחירום
      </div>
      <button @click="nextPage" class="btns" id="start-lomda-btn"> צאו לדרך </button>
    </div>
  </div>
</template>
 
<script>
export default {
  name: "open-screen",
  components: {},
  data() {
    return {};
  },
  mounted() {

    setTimeout(() => {
      document.getElementById(`logoGif`).style.display = "none";
      document.getElementById(`logo`).style.display = "block";
    }, 4000);
    setTimeout(() => {
      document.getElementById(`logo`).style.top = "3vh";
      document.getElementById(`logo`).style.left = "34vh";
      document.getElementById(`logo`).style.width = "36vw";
    }, 4200);
    setTimeout(() => {
      document.getElementById(`open-text`).style.opacity = "1";
    }, 4500);
  },
  methods: {
    nextPage() {
            this.$emit('next-page');
        },
  },
};
</script>

<style scoped>
#open-screen {
  height: 100vh;
  width: 100vw;
  background-image: url("../assets/imgs/Bg1.png");
  background-size: 100% 100%;
  background-repeat: no-repeat;
  overflow: hidden;
}

.shadow {
  display: block;
  position: absolute;
  height: 100vh;
  width: 100vw;
  background-color: rgba(255, 255, 255, 0.589);
  z-index: 1;
}

#logoGif {
  z-index: 2;
  position: absolute;
  top: 32vh;
  left: 5vh;
  width: 45vh;
}

#logo {
  display: none;
  z-index: 2;
  position: absolute;
  top: 36.5vh;
  left: 6vh;
  width: 41vh;
  transition: top 1s ease, left 1s ease, width 1s ease;
}

.titles {
  font-family: Karantina;
  position: absolute;
  color: #175a85;
  z-index: 2;
  text-align: center;
}

#open-div1 {
  top: 17vh;
  left: 16vw;
  font-size: 11vmin;
  width: 68vw;
}

#open-div2 {
  top: 43vh;
  left: 16vw;
  font-size: 8vmin;
  width: 68vw;
}

.btns {
  position: absolute;
  font-family: Karantina;
}

#start-lomda-btn {
  z-index: 3;
  width: 27vw;
  top: 67vh;
  height: 15vw;
  left: 34vw;
  font-size: 7vmin;
  border-radius: 2vh;
  border: none;
  background-color: #175a85;
  color: white;
}

#open-text{
  opacity: 0;
  transition: opacity 2s ease;
}
</style>
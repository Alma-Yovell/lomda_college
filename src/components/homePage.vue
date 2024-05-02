<template>
    <div id="home-page">
        <img :src="require('@/assets/imgs/collegeLogo.png')" alt="logo" id="logo" />

    </div>
</template>
   
<script>
export default {
    name: "home-page",
    components: {},
    data() {
        return {};
    },
    methods: {
        nextPage() {
            this.$emit('next-page');
        },
    },
};
</script>
  
<style scoped>
#home-page {
    height: 100vh;
    width: 100vw;
    background-image: url("../assets/imgs/Bg2.png");
    background-size: 100% 100%;
    background-repeat: no-repeat;
    overflow: hidden;
}

#logo {
    position: absolute;
    top: 3vh;
    left: 34vh;
    width: 20vh;
}
</style>
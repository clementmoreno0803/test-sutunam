<template>
  <bandeau></bandeau>
  <header>
    <Nav></Nav>
    <Dropdown></Dropdown>
  </header>
  <router-view />
</template>
<script>
import Bandeau from "@/components/Bandeau.vue";
import Dropdown from "@/components/NavDropdown.vue";
import Nav from "@/components/Nav.vue";
export default {
  name: "App",
  components: {
    Bandeau,
    Dropdown,
    Nav,
  },
};
</script>
<style>
:root {
  --bandeau: #154331;
  --white: #fff;
  --dark-green: #154331;
  --pine: #396755;
  --cloudy-green: #c5ddd1;
  --colormap-getcolorswarm-grey: #e8f2ed;
  --white: #fff;
  --gold: #aa800f;
  --light-gold: #dec480;
  --sand: #f3e4c3;
  --light-sand: #f8eeda;
  --brownish-grey: #646363;
  --warm-grey: #9a9494;
  --pink: #e187a3;
  --faded-pink: #f3e0e7;
  --putty: #c6d2b1;
  --light-puttylight-putty: #dfe8e0;
  --cloudy-blue: #badfd8;
  --light-blue: #ebf6f3;
  --brownish-grey-60: rgba(100, 99, 99, 0.6);
}
@import url("https://fonts.googleapis.com/css2?family=Abhaya+Libre:wght@600&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Fira+Sans&display=swap");

@font-face {
  font-family: MetaPro;
  src: local(MetaPro-Light),
    url(../src/assets/fonts/MetaPro-Light_30262.ttf) format("truetype");
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
}

.h1 {
  font-family: "Abhaya Libre", serif;
  font-size: 58px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.38;
  letter-spacing: normal;
  text-align: left;
  color: var(--dark-green);
}

.h2 {
  font-family: "Abhaya Libre", serif;
  font-size: 48px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 0.42;
  letter-spacing: normal;
  text-align: left;
  color: var(--dark-green);
}

.h3 {
  font-family: "Abhaya Libre", serif;
  font-size: 36px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.67;
  letter-spacing: normal;
  text-align: left;
  color: var(--dark-green);
}

.h4 {
  font-family: "Abhaya Libre", serif;
  font-size: 20px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: normal;
  text-align: center;
  color: var(--dark-green);
}

h5 {
  font-family: "Abhaya Libre", serif;
  font-size: 18px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.11;
  letter-spacing: normal;
  text-align: center;
  color: var(--white);
}

.OVERTITLE-UPPERCASE {
  font-family: MetaPro;
  font-size: 18px;
  font-weight: 300;
  font-stretch: normal;
  font-style: normal;
  line-height: 4.44;
  letter-spacing: 5.4px;
  text-align: left;
  color: var(--brownish-grey);
}

.Chap {
  font-family: "metapro-normal-regular", sans-serif;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.88;
  letter-spacing: 0.8px;
  text-align: left;
  color: var(--brownish-grey);
}

a,
h6 {
  font-family: "Fira Sans";
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: 0.7px;
  text-align: left;
  color: var(--brownish-grey);
  text-decoration: none;
  position: relative;
}

p {
  font-family: "metapro-normal-regular", sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: 0.7px;
  text-align: left;
  color: var(--brownish-grey);
}

.Mentions {
  font-family: "metapro-normal-regular", sans-serif;
  font-size: 12px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.67;
  letter-spacing: 0.6px;
  text-align: left;
  color: var(--brownish-grey);
}
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  text-align: center;
}
.container {
  width: calc(100% - 160px);
  margin: 0 auto;
  height: 100%;
  display: flex;
}
#nav {
  position: sticky;
  z-index: 5;
  background: white;
}
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

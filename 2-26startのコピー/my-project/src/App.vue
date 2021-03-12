<template>
  <div id="app">
    <Header />
    <HeaderImage />
    <ConceptBox />
    <Test1 />
  </div>
</template>

<script>
import Header from "./components/Header";
import HeaderImage from "./components/HeaderImage";
import ConceptBox from "./components/ConceptBox";
import Test1 from "./components/Test1";
export default {
  name: "App",
  components: {
    Header,
    HeaderImage,
    ConceptBox,
    Test1,
  },
};
</script>

<style>
html {
  font-family: "Noto Sans JP", sans-serif;
}

body {
  overflow: hidden;
  height: 1000px;
}
</style>

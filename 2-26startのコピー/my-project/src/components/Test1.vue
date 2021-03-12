<template>
  <div class="hello">
    <p v-scroll="handleScroll2">kkkk</p>
    <div class="test11" v-scroll="handleScroll1">aaaaaaaaa</div>
    <div class="test12" v-scroll="handleScroll1"></div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: () => ({
    test: false,
    data: 0,
  }),

  methods: {
    handleScroll1: function(evt, el) {
      if (window.scrollY > 50) {
        el.setAttribute("style", "display: block");
      }
      return window.scrollY > 100;
    },
    handleScroll2: function(evt, el) {
      if (window.scrollY > 50) {
        el.setAttribute("class", "red");
      }
      return window.scrollY > 50;
    },
    handleScroll3: function() {},
  },
  // mounted() {
  //   console.log("ssssss");
  //   addEventListener("scroll", getInfo);
  //   function getInfo() {
  //     this.data = window.scrollY;
  //     if (window.scrollY > 50) {
  //       this.test = !this.test;
  //       console.log("test");
  //     }
  //     console.log(this.data);
  //   }
  // },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.hello {
  height: 1000px;
}

.test {
  opacity: 1;
  margin-top: 100px;
  width: 100px;
  height: 100px;
  background-color: red;
}

.red {
  color: blue;
}

.test11 {
  display: none;
  width: 100px;
  height: 100px;
  background-color: black;
  animation: test11 ease 2s forwards;
  margin: 0 auto;
}

.test12 {
  display: none;
  width: 100px;
  height: 2px;
  background-color: red;
  animation: test12 ease 2s forwards;
}

@keyframes test11 {
  0% {
    margin-bottom: 50px;
    opacity: 0;
  }
  100% {
    margin-bottom: 0px;
    opacity: 1;
  }
}

@keyframes test12 {
  0% {
    width: 0px;
    opacity: 0;
  }
  100% {
    width: 100px;
    opacity: 1;
  }
}
</style>

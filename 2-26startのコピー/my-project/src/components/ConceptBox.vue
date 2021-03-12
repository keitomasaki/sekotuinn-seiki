<template>
  <div class="concept-box">
    <div class="title-box-wrapper">
      <div class="title-box" v-scroll="handleScroll1">
        <h3 class="title-box-text">Concept</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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
  },
};
</script>

<style>
.concept-box {
  width: 100%;
  height: auto;
  padding-top: 30px;
  border: 1px solid black;
}

.title-box-wrapper {
  width: 40%;
  /* height: auto; */
  height: 50px;
  border: 1px solid red;
  margin: 0 auto;
  position: relative;
}

.title-box {
  display: none;
  width: auto;
  height: auto;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>

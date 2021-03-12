<template>
  <div>
    <v-navigation-drawer class="navi" v-model="drawer" absolute temporary>
      <div class="flex">
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
        <div class="test">
          <button class="button" @click="test">aaaa</button>
        </div>
      </div>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  props: ["drawer"],
  data: () => ({
    group: null,
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
  methods: {
    test() {
      console.log("kkkkkkkkkkk");
    },
  },
};
</script>

<style>
.navi {
  height: 100% !important;

  background-color: #191970 !important;
}

p {
  text-align: center;
  color: white;
}

/* .button {
  width: 150px;
  height: 70px;
  position: relative;
  border: 1px solid white;
  overflow: hidden;
  color: white;
} */

.button {
  width: 100%;
  height: 100%;
  position: relative;
  border: 1px solid white;
  overflow: hidden;
  color: white;
}

.test {
  width: 110px;
  height: 60px;
  margin: 0 auto;
  margin-bottom: 50px;
  text-align: center;
}

.flex {
  height: 100%;
}

.button:hover {
  color: black;
}

.button::before {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
  content: "";
  background: white;
  transform-origin: right top;
  transform: scale(0, 1);
  transition: transform 0.2s;
}
.button:hover::before {
  transform-origin: left top;
  transform: scale(1, 1);
}
</style>

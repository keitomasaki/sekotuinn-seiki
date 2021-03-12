<template>
  <v-container>
    <v-row class="row1" justify="center" align-content="center">
      <v-col cols="6">
        <div class="headerBox-left">
          <img class="img-box1" :src="logoblack" alt="" />
          <div class="header_title_box">
            <h5>手と手整骨院</h5>
          </div>
        </div>
      </v-col>

      <v-col cols="6" align-self="end">
        <div class="header-right">
          <button class="btn">ご予約はこちら</button>
          <HabergerMenu class="hamberger-menu" />
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import logoblack from "../assets/logoblack.png";
import HabergerMenu from "./HabergerMenu";

export default {
  components: {
    HabergerMenu,
  },
  data: () => ({
    logoblack: logoblack,
  }),
};
</script>

<style scoped>
h5 {
  font-size: 14px !important;
}

.container {
  height: 64px;
}

.headerBox-left {
  height: 34px;
  display: flex;
}

.header-right {
  height: 34px;
  display: flex;
  justify-content: flex-end;
}

.header_title_box {
  height: inherit;
  width: auto;
  line-height: 34px;
  margin-left: 8px;
}

.btn {
  height: inherit;
  width: 112px;
  background-color: #71bd8c;
  border-radius: 15px;
  font-size: 12px;
}

.btn:focus {
  outline: none;
}

.navi-icon {
  margin-left: 7px;
}

.img-box1 {
  height: 36px !important;
  width: 35px !important;
}
</style>

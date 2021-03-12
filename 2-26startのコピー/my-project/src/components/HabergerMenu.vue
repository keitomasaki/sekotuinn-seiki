<template>
  <div class="HambergerMenu">
    <div class="btn" @click="toggle">
      <div class="icon-wrapper">
        <font-awesome-icon
          class="align-justify-btn"
          icon="align-justify"
          size="lg"
        />
      </div>
    </div>
    <Drawer
      @close="toggle"
      align="right"
      :closeable="true"
      :maskClosable="true"
    >
      <div v-if="open">content here</div>
    </Drawer>
  </div>
</template>

<script>
import Drawer from "vue-simple-drawer";

export default {
  name: "HambergerMenu",
  components: {
    Drawer,
  },
  data() {
    return {
      open: false,
    };
  },
  methods: {
    toggle() {
      this.open = !this.open;
    },
  },
};
</script>
<style scoped lang="scss">
.vue-simple-drawer {
  width: 300px;
}
.btn {
  min-width: 30px;
}

.icon-wrapper {
  width: inherit;
  height: 100%;
  position: relative;
}

.align-justify-btn {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.HambergerMenu {
  display: flex;
  align-content: center;
}

.leftright {
  background-color: red !important;
}
</style>

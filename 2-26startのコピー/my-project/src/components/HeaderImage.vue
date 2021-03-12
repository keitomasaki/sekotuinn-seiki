<template>
  <div class="header-image">
    <img class="image" :src="Group1" alt="" />
  </div>
</template>

<script>
import Group1 from "../assets/Group1.png";
export default {
  data: () => ({
    Group1: Group1,
  }),
};
</script>

<style>
.header-image {
  object-fit: cover;
  height: calc(100vw * 0.75);
}

.image {
  width: 100%;
  height: inherit;
  object-fit: cover;
}
</style>

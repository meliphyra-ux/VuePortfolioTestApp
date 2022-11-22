<script>
export default {
  props: {
    top: Number,
    left: Number,
    rotate: Number,
  },
  data() {
    return {
      blobShow: false,
    };
  },
  mounted() {
    setTimeout(() => (this.blobShow = true), 50);
  },
};
</script>
<template>
  <div
    class="blub"
    :style="{
      top: top + '%',
      left: left + '%',
      transform: blobShow ? `rotate(${rotate}deg)` : 'translate(-50%, -50%)',
      opacity: blobShow ? '1' : '0',
      transformOrigin: blobShow ? 'top left' : 'center',
    }"
  ></div>
</template>
<style scoped>
.blub {
  position: absolute;
  z-index: -1;
  border-radius: 15px 50%;
  min-width: 250px;
  min-height: 250px;
  /* filter: blur(rem); */
  box-shadow: 0px 0px 60px 0px #58ffa0;
  transition: all 1s ease;
  background: -webkit-linear-gradient(60deg, #289ab9, #12be03);
  text-align: center;
}
</style>

<script>
export default {
  data() {
    return {
      mousePositionX: 0,
      mousePositionY: 0,
    };
  },
  mounted() {
    console.log(this.mousePositionX, this.mousePositionY);
  },
  // methods: {
  //   logPosition(event) {
  //     setTimeout(() => {
  //       this.mousePositionX = event.clientX;
  //       this.mousePositionY = event.clientY;
  //     }, 0);
  //   },
  // },
};
</script>
<!-- @mousemove="logPosition($event)" -->
<template>
  <main>
    <div>
      <h2>Welcome to the world of web development!</h2>
    </div>
    <!-- <div
      class="blub"
      :style="{
        transform: `translate(${mousePositionX - 125}px, ${
          mousePositionY - 125
        }px)`,
      }"
    >
      Blub
    </div> -->
    <div
      class="blub"
      :style="{
        top: '50%',
        left: '50%',
        transform: 'rotate(135deg) ',
      }"
    ></div>
    <div
      class="blub"
      :style="{
        top: '50%',
        left: '50%',
        transform: 'rotate(120deg) ',
      }"
    ></div>
    <div
      class="blub"
      :style="{
        top: '50%',
        left: '50%',
        transform: 'rotate(150deg)',
      }"
    ></div>
  </main>
</template>

<style scoped>
h2 {
  color: #f2f2f2;
  text-align: center;
}
main {
  display: flex;
  position: relative;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  min-height: calc(100vh - 60px);
  overflow: hidden;
}
.blub {
  position: absolute;
  z-index: -1;
  border-radius: 15px 50%;
  min-width: 350px;
  min-height: 350px;
  /* filter: blur(rem); */
  box-shadow: 0px 0px 60px 0px #58ffa0;
  transform-origin: left top;
  background: -webkit-linear-gradient(60deg, #289ab9, #12be03);
  text-align: center;
}
</style>

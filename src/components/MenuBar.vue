<script>
export default {
  data() {
    return {
      MenuBarLeft: 0,
    };
  },
  mounted() {
    this.updateLeftPosition();
    window.addEventListener('resize', this.updateLeftPosition);
  },
  unmounted() {
    window.removeEventListener('resize', this.updateLeftPosition);
  },
  methods: {
    updateLeftPosition() {
      const barWidth = this.$refs.Element.offsetWidth;

      this.MenuBarLeft = `calc(50% - ${barWidth / 2}px)`;
    },
    openGithub() {
      window.open('https://www.github.com/DylanAkp');
    },
    openTwitter() {
      window.open('https://www.twitter.com/DylanAkp');
    },
    openSourceCode() {
      window.open('https://github.com/DylanAkp/Portfolio');
    },
  },
};
</script>

<template>
  <div class="bar no-select" ref="Element" :style="{ left: MenuBarLeft }">
    <div>Dylan AKPINAR</div>
    <q-icon
      @click="openGithub"
      class="icon-click"
      name="ion-logo-github"
      color="black"
      size="23px"
      title="GitHub"
    />
    <q-icon
      @click="openTwitter"
      class="icon-click"
      name="ion-logo-twitter"
      color="black"
      size="23px"
      title="Twitter/X"
    />
    <q-icon
      @click="openSourceCode"
      style="margin-left: 15px"
      class="icon-click"
      name="ion-code"
      color="black"
      size="23px"
      title="Portfolio Source Code"
    />
  </div>
</template>

<style scoped>
.icon-click {
  cursor: pointer;
}

.icon-click:hover {
  transform: scale(1.1);
}
.bar {
  gap: 10px;
  padding-right: 10px;
  padding-left: 10px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  width: auto;
  height: 30px;
  top: 20px;
  background-color: #ffffff;
  opacity: 0.98;
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  -moz-backdrop-filter: blur(10px);
  -ms-backdrop-filter: blur(10px);
  -o-backdrop-filter: blur(10px);
  box-shadow: 0 0 10px #dbdbdb;
  position: fixed;
  border-radius: 15px;
}
</style>

<script>
export default {
  name: 'ProfileComponent',
};
</script>

<template>
  <div class="bubble">
    <div class="about">
      <div style="font-weight: 600; font-size: x-large">Dylan AKPINAR</div>
      <img class="profile" src="~assets/picture.jpeg" />
      <div>Software Engineer</div>
    </div>
    <div class="description">
      My name is Dylan AKPINAR, I'm an Epitech student in my 4th year.
      <br />On my free time, I like to customize my devices software<br />from
      Linux on my Switch to rooting and trying new GSIs on my phone. <br />I
      want to work in the field of mobile development and IoT.
    </div>
  </div>
</template>

<style scoped>
@media screen and (min-width: 1048px) {
  .bubble {
    padding-left: 70px;
  }
}

.profile {
  border-radius: 25px;
  width: auto;
  height: 150px;
}

.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 10px;
}
</style>

<script>
export default {
  name: 'ContactInformations',
  methods: {
    MailTo() {
      window.open('mailto:contact@dylanakp.dev');
    },
    CopyPhone() {
      navigator.clipboard.writeText('07 81 48 61 38');
    },
    GoToLinkedIn() {
      window.open('https://www.linkedin.com/in/dylan-akpinar-2454261b8/');
    },
  },
};
</script>

<template>
  <div class="bubble">
    <div class="contact">
      <div style="font-weight: 600; font-size: x-large">Contact</div>
      <div style="text-align: center">
        Want to work together ?<br />
        <div style="font-style: italic">Contact me !</div>
      </div>
      <div class="clickable" @click="MailTo">
        <q-icon name="ion-mail" /> contact@dylanakp.dev
      </div>
      <div class="clickable" @click="CopyPhone">
        <q-icon name="ion-call" /> (+33) 07 81 48 61 38
      </div>
      <div class="clickable" @click="GoToLinkedIn">
        <q-icon name="ion-logo-linkedin" /> Dylan AKPINAR
      </div>
    </div>
  </div>
</template>

<style scoped>
.bubble {
  width: 30vw;
  height: 100% !important;
  justify-content: center;
}
.clickable:hover {
  transform: scale(1.1);
  cursor: pointer;
}
.contact {
  display: flex;
  flex-direction: column;
  align-self: baseline;
  align-items: center;
  justify-content: center;
  gap: 10px;
}
</style>

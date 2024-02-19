<template>
  <main>
    <audio-recorder style="background-color: #ffffffde; color: black;" upload-url="YOUR_API_URL" :attempts="3" :time="2"
      :headers="headers" :before-recording="callback" :pause-recording="callback" :after-recording="callback"
      :select-record="callback" :before-upload="callback" :successful-upload="callback" :failed-upload="callback" />
  </main>
</template>

<script>
export default {
  methods: {
    callback(data) {
      console.debug(data)
    }
  }
}
</script>

<style scoped>
main {
  text-align: center;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(to right, #0f2027c1, #203a43b1, #2c5364), url('../assets/bg.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
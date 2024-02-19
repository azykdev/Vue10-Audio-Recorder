<template>
  <main>
    <audio-recorder upload-url="YOUR_API_URL" :attempts="3" :time="2" :headers="headers" :before-recording="callback"
      :pause-recording="callback" :after-recording="callback" :select-record="callback" :before-upload="callback"
      :successful-upload="callback" :failed-upload="callback" />
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
}
</style>
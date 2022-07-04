<template>
  <div class="timer-holder">
    <p>{{ title }}</p>

    <p font="mono" style="font-size: 32px">
      {{ timeLeft }}
    </p>
    <button
      border="gray-400 opacity-50"
      p="1"
      font="mono"
      outline="!none"
      hover:bg="gray-400 opacity-20"
      style="font-size: 14px; margin-bottom: 0; padding-bottom: 0"
      @click="startTimer()"
      v-if="!timerStarted"
    >
      Start Timer
    </button>
    <img
      src="/assets/images/loading/moving-cube.gif"
      style="height: 50%; resize-mode: contain; width: 50%"
      v-if="timerStarted"
    />
  </div>
</template>

<style scoped>
.timer-holder {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>


<script>
export default {
  props: ["countdownTime", "title"],
  data() {
    return {
      timeLeft: `${this.countdownTime}:00`,
      secondsLeft: this.countdownTime * 60,
      timerStarted: false,
    };
  },
  methods: {
    startTimer() {
      //   this.displayTimeLeft(this.countdownTime * 60);
      this.timerStarted = true;
      const now = Date.now();
      const end = now + this.secondsLeft * 1000;
      this.displayTimeLeft(this.secondsLeft);
      this.countdown(end);
    },
    countdown(end) {
      intervalTimer = setInterval(() => {
        const secondsLeft = Math.round((end - Date.now()) / 1000);

        if (secondsLeft === 0) {
          this.endTime = 0;
        }

        if (secondsLeft < 0) {
          clearInterval(intervalTimer);
          return;
        }
        this.displayTimeLeft(secondsLeft);
      }, 1000);
    },
    displayTimeLeft(secondsLeft) {
      const minutes = Math.floor((secondsLeft % 3600) / 60);
      const seconds = secondsLeft % 60;

      this.timeLeft = `${zeroPadded(minutes)}:${zeroPadded(seconds)}`;
    },
  },
};

function zeroPadded(num) {
  // 4 --> 04
  return num < 10 ? `0${num}` : num;
}

function hourConvert(hour) {
  // 15 --> 3
  return hour % 12 || 12;
}
</script>
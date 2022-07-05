<template>
  <div class="timer-holder">
    <div class="text-holder">
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
    </div>

    <img
      src="/assets/images/loading/moving-circle.gif"
      class="circular-img"
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

.text-holder {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  margin-right: auto;
  margin-left: auto;
  margin-top: auto;
  margin-bottom: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 200px;
  width: 200px;
  z-index: 2;
}

.circular-img {
  position: absolute;
  top: 0;
  bottom: 0;
  height: 400px;
  width: 400px;
  left: 0;
  right: 0;
  margin-right: auto;
  margin-left: auto;
  margin-top: auto;
  margin-bottom: auto;
  z-index: 1;
  object-fit: contain;
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
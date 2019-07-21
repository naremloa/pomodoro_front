<template>
  <div class="countdown">
    <div class="num">{{getDisplayNum}}</div>
    <div class="button-group">
      <div class="bell-btn"></div>
      <div
        class="operate-btn btn"
        @click="startCountdown" />
      <div class="cancel-btn"></div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

const getTime = () => (new Date()).getTime();

const getTimeDisplay = (num: number) => {
  const date = new Date(num);
  const m = date.getMinutes().toString().padStart(2, '0');
  const s = date.getSeconds().toString().padStart(2, '0');
  return `${m}:${s}`;
};

@Component({
  components: {
  },
})
export default class Countdown extends Vue {
  systemTime: number = 0

  systemIntervalId: number|null = null

  countdownFlag: boolean = false

  targetTime: number = 0

  type: 0|1 = 1

  get getDisplayNum() {
    if (!this.countdownFlag) return this.type === 1 ? '25:00' : '05:00';
    return getTimeDisplay(this.targetTime - this.systemTime);
  }

  get countdownZone() {
    return 1000 * 60 * (this.type === 1 ? 25 : 5);
  }

  startCountdown() {
    if (this.systemIntervalId !== null) {
      clearInterval(this.systemIntervalId);
      this.systemIntervalId = null;
    }
    this.targetTime = getTime() + this.countdownZone;
    this.systemTime = getTime();
    this.systemIntervalId = setInterval(() => { this.systemTime = this.systemTime + 1000; }, 1000);
    this.countdownFlag = true;
  }
}
</script>

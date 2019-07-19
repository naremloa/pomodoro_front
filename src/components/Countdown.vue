<template>
  <div class="countdown">
    <div class="num">25:00</div>
    <div class="button-group">
      <div class="bell-btn"></div>
      <div class="operate-btn"></div>
      <div class="cancel-btn"></div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {
  },
})
export default class Countdown extends Vue {}
</script>

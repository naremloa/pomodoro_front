<template>
  <div class="footer">
    <div style="max-height: 260px">
      <img :src="{ 0: green, 1: orange }[type]" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

const orange = require('@/assets/tomato--orange.svg');
const green = require('@/assets/tomato--green.svg');

@Component({
  components: {
  },
})
export default class Footer extends Vue {
  type: 0|1 = 0

  green: any = green

  orange: any = orange
}
</script>

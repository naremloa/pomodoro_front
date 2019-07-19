<template>
  <div class="interf">
    <Countdown />
    <Todolist />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Countdown from './Countdown.vue';
import Todolist from './Todolist.vue';

@Component({
  components: {
    Countdown,
    Todolist,
  },
})
export default class Interf extends Vue {}
</script>

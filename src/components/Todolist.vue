<template>
  <div class="todolist">
    <template v-if="type === 0">
      <div class="restitem">
        <div>休息，</div>
        <div>是為了下一次的努力。</div>
      </div>
    </template>
    <template v-else-if="type === 1">
      <div class="todoitem">
        <div class="todoitem-pre" />
        <div class="todoitem-describ">
          <div>構思番茄鐘 UI 介面</div>
          <div class="moon-group">
            <div class="moon"><div class="shader" style="left: 0px"></div></div>
            <div class="moon"><div class="shader" style="left: 0px"></div></div>
            <div class="moon"><div class="shader" style="left: 0px"></div></div>
            <div class="moon"><div class="shader" style="left: -5px"></div></div>
          </div>
        </div>
      </div>
      <div class="todoitem">
        <div class="todoitem-pre" />
        <div class="todoitem-describ">
          <div>學習 javascript</div>
        </div>
      </div>
      <div class="todoitem">
        <div class="todoitem-pre" />
        <div class="todoitem-describ">
          <div>學習 網頁切版</div>
        </div>
      </div>
      <div class="todoitem">
        <div class="todoitem-pre" />
        <div class="todoitem-describ">
          <div>設計番茄鐘 UI 介面</div>
        </div>
      </div>
    </template>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {
  },
})
export default class Todolist extends Vue {
  type: 0|1 = 0
}
</script>

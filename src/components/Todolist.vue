<template>
  <div class="todolist">
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

  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {
  },
})
export default class Todolist extends Vue {}
</script>

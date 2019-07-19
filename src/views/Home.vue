<template>
  <div class="container">
    <Sidebar />
    <Content />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Sidebar from '@/components/Sidebar.vue';
import Content from '@/components/Content.vue';

@Component({
  components: {
    Sidebar,
    Content,
  },
})
export default class Home extends Vue {}
</script>

<template>
  <div class="content">
    <Header />
    <div class="main">
      <Interf />
      <Footer ref="footer" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Interf from './Interf.vue';
import Footer from './Footer.vue';
import Header from './Header.vue';

@Component({
  components: {
    Interf,
    Footer,
    Header,
  },
})
export default class Content extends Vue {
  mounted() {
    console.log('check', this.$refs.footer);
  }
}
</script>

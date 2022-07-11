<template>
  <div class="guide-wrap">
    <Nuxt />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
    components: {}
})
export default class HomePage extends Vue {
 
}
</script>
<style lang="scss" scoped>
  .guide-wrap {
    padding:2rem;
  }
</style>


<template>
  <div>
    <nav>
      <ul>
        <li><a href="#"></a></li>
      </ul>
    </nav>
    <Nuxt />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
    components: {}
})
export default class HomePage extends Vue {
  navList:any = ["메뉴1", "메뉴2"]
}
</script>


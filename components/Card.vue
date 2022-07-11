<template>
  <div>
    {{title}}
  </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator'

@Component({
    components: {},
    props: ['title'],
})
export default class HomePage extends Vue {}
// export default {
//   name: 'BuefyCard',
//   props: {
//     title: {
//       type: String,
//       required: true
//     },
//     icon: {
//       type: String,
//       required: true
//     }
//   }
// }
</script>




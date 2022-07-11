<template>
  <section class="section">
    <card
        title="Responsive"
      >
    </card>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Card from '~/components/Card.vue'

@Component({
    components: {Card}
})
export default class HomePage extends Vue {}
</script>

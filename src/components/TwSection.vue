<template>
  <section class="my-4 text-center">
    <slot />
  </section>
</template>

<script>
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class TwSection extends Vue {}
</script>


<template>
  <button class="rounded mx-1 border-2" :class="className">
    <slot />
  </button>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({})
export default class TwButton extends Vue {
  @Prop({ default: "regular" })
  size!: string;

  @Prop({ default: "primary" })
  variant!: string;

  get className() {
    return `${this.sizeClass} ${this.variantClass}`;
  }

  get sizeClass() {
    switch (this.size) {
      case "regular": {
        return "py-2 px-4";
      }

      case "large": {
        return "py-3 px-6 text-lg";
      }

      case "small": {
        return "py-px px-2 text-sm";
      }
    }
  }

  get variantClass() {
    switch (this.variant) {
      case "primary": {
        return "text-white bg-gradient-to-b from-blue-400 to-blue-500 border-blue-400";
      }

      case "secondary": {
        return "text-blue-400 border-blue-400";
      }

      case "error": {
        return "text-white bg-gradient-to-b from-red-400 to-red-500 border-red-400";
      }
    }
  }
}
</script>


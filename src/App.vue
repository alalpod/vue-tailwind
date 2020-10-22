<template>
  <div>
    <tw-section>
      <h2>Button size</h2>
      <tw-button>Button</tw-button>
      <tw-button size="large">Button</tw-button>
      <tw-button size="small">Button</tw-button>
    </tw-section>
    <tw-section>
      <h2>Button variant</h2>
      <tw-button>Button</tw-button>
      <tw-button variant="secondary">Button</tw-button>
      <tw-button variant="error">Button</tw-button>
    </tw-section>
  </div>
</template>

<script>
import { Component, Vue } from "vue-property-decorator";
import TwSection from "./components/TwSection";
import TwButton from "./components/TwButton";

@Component({
  components: { TwSection, TwButton },
})
export default class App extends Vue {}
</script>


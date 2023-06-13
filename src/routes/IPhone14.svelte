<script lang="ts">
  import Iphone14Default from "./iphone14-default.svelte";
  import Iphone14SideRight from "./iphone14-side-right.svelte";
  import Iphone14SideLeft from "./iphone14-side-left.svelte";

  export let type: string = "default";
  export let screen: any;
  
  export let screenHeight: string;
  export let screenWidth: string;

  export let skewY: any = undefined;
  export let translateY: any = undefined;
  export let translateX: any = undefined;
</script>

{#if type === "default"}
  <Iphone14Default {screen} {screenWidth} {screenHeight} />
{:else if type === "side-right"}
  <Iphone14SideRight
    {screen}
    {screenWidth}
    {screenHeight}
    skewY={skewY ? skewY : "13deg"}
    translateX={translateX ? translateX : "-15px"}
    translateY={translateY ? translateY : "5px"}
  />
{:else if type === "side-left"}
  <Iphone14SideLeft
    {screen}
    {screenWidth}
    {screenHeight}
    skewY={skewY ? skewY : "-13deg"}
    translateX={translateX ? translateX : "15px"}
    translateY={translateY ? translateY : "5px"}
  />
{/if}

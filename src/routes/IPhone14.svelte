<script lang="ts">
  import Iphone14Default from "./iphone14-default.svelte";
  import Iphone14SideRight from "./iphone14-side-right.svelte";
  import Iphone14SideLeft from "./iphone14-side-left.svelte";
  import Iphone14HoverLeft from "./iphone14-hover-left.svelte";
  import Iphone14HoverRight from "./iphone14-hover-right.svelte";
  import Iphone14FrontAndBack from "./iphone14-front-and-back.svelte";

  export let type: string = "default";
  export let screen: any;

  export let scale: any = undefined;
  export let screenHeight: any = undefined;
  export let screenWidth: any = undefined;

  export let skewX: any = undefined;
  export let skewY: any = undefined;
  export let translateY: any = undefined;
  export let translateX: any = undefined;
  export let rotate: any = undefined;
</script>

{#if type === "default"}
  <Iphone14Default
    {screen}
    scale={scale ? scale : "100%"}
    screenWidth={screenWidth ? screenWidth : "38%"}
    screenHeight={screenHeight ? screenHeight : "82.5%"}
    skewX={skewX ? skewX : "0deg"}
    skewY={skewY ? skewY : "0deg"}
    translateX={translateX ? translateX : "1px"}
    translateY={translateY ? translateY : "0px"}
  />
{:else if type === "side-right"}
  <Iphone14SideRight
    {screen}
    scale={scale ? scale : "100%"}
    screenWidth={screenWidth ? screenWidth : "25%"}
    screenHeight={screenHeight ? screenHeight : "66%"}
    skewX={skewX ? skewX : "0deg"}
    skewY={skewY ? skewY : "13deg"}
    translateX={translateX ? translateX : "-15px"}
    translateY={translateY ? translateY : "5px"}
  />
{:else if type === "side-left"}
  <Iphone14SideLeft
    {screen}
    scale={scale ? scale : "100%"}
    screenWidth={screenWidth ? screenWidth : "25.5%"}
    screenHeight={screenHeight ? screenHeight : "66%"}
    skewX={skewX ? skewX : "0deg"}
    skewY={skewY ? skewY : "-13deg"}
    translateX={translateX ? translateX : "14px"}
    translateY={translateY ? translateY : "7px"}
  />
{:else if type === "hover-right"}
  <Iphone14HoverRight
    {screen}
    scale={scale ? scale : "100%"}
    screenWidth={screenWidth ? screenWidth : "25%"}
    screenHeight={screenHeight ? screenHeight : "53%"}
    rotate={rotate ? rotate : "37.12deg"}
    skewX={skewX ? skewX : "-25deg"}
    skewY={skewY ? skewY : "0deg"}
    translateX={translateX ? translateX : "-15px"}
    translateY={translateY ? translateY : "-25px"}
  />
{:else if type === "hover-left"}
  <Iphone14HoverLeft
    {screen}
    scale={scale ? scale : "100%"}
    screenWidth={screenWidth ? screenWidth : "25%"}
    screenHeight={screenHeight ? screenHeight : "53%"}
    rotate={rotate ? rotate : "-37.12deg"}
    skewX={skewX ? skewX : "25deg"}
    skewY={skewY ? skewY : "0deg"}
    translateX={translateX ? translateX : "28px"}
    translateY={translateY ? translateY : "-11px"}
  />
{:else if type === "front-and-back"}
  <Iphone14FrontAndBack
    {screen}
    scale={scale ? scale : "100%"}
    screenWidth={screenWidth ? screenWidth : "29%"}
    screenHeight={screenHeight ? screenHeight : "61.5%"}
    rotate={rotate ? rotate : "0deg"}
    skewX={skewX ? skewX : "0deg"}
    skewY={skewY ? skewY : "0deg"}
    translateX={translateX ? translateX : "101px"}
    translateY={translateY ? translateY : "7.5px"}
  />
{/if}

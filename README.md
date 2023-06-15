# Svelte Mockups

This library is meant to provde a simple solution for mockups in SvelteKit.

## Installation

```bash
npm install svelte-mockups
```

## Usage

> All of the parameters have been set to fit a screenshot with the dimesions 461px x 1000px (WxH) and an aspect ratio must be 19.5:9.
> If you use a screen-image with different dimensions, you might need to adjust the parameters: most commonly screenWidth, screenHeight, translateX and translateY!

Usage with a screenshot thats 461px x 1000px:

```html
<script lang="ts">
  import IPhone14 from "./IPhone14.svelte";
  import screenshot from "$lib/assets/screenshot.png";
</script>

<IPhone14 screen="{screenshot}" />

<IPhone14 screen="{screenshot}" type="side-right" />
<IPhone14 screen="{screenshot}" type="side-left" />

<IPhone14 screen="{screenshot}" type="hover-right" />
<IPhone14 screen="{screenshot}" type="hover-left" />
```

## Parameters

- scale
- screenHeight
- screenWidth
- skewX
- skewY
- translateY
- translateX
- rotate

```html
<script lang="ts">
  import IPhone14 from "./IPhone14.svelte";
  import screenshot from "$lib/assets/screenshot.png";
</script>

<IPhone14
  screen="{screenshot}"
  type="hover-left"
  scale="90%"
  rotate="0deg"
  screenHeight="100%"
  screenWidth="100%"
  skewX="10deg"
  skewY="10deg"
  translateX="20px"
  translateY="20px"
/>
```

## The mockups used in this project are from [mockups-design.com](https://mockups-design.com/free-iphone-14-pro-mockup/). They were Slightly edited to fit better for this project.

## They are <u>royalty free</u> and can be used commercially as specified in their [License](https://mockups-design.com/license/).

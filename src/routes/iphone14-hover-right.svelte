<script lang="ts">
  export let skewX: any;
  export let skewY: any;
  export let translateY: any;
  export let translateX: any;
  export let rotate: any;

  export let scale: any;
  export let screen: any;
  export let screenWidth: string;
  export let screenHeight: string;
</script>

<div class="container" style="--scale:{scale};">
  <div class="screenMask">
    <img
      src={screen}
      alt="screen"
      class="screen"
      width={screenWidth}
      height={screenHeight}
      style="--rotate:{rotate};--skewX:{skewX};--skewY:{skewY};--translateY:{translateY};--translateX:{translateX};"
    />
  </div>
  <img src="/iphone14_hover_right.png" alt="phone" class="phone" />
</div>

<style>
  .container {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 900px;
    height: 900px;
    transform: scale(var(--scale));
  }

  .screenMask {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 900px;
    height: 900px;
    -webkit-mask: url("/iphone14_hover_right_mask.png") no-repeat;
  }

  .phone {
    width: 900px;
    position: absolute;
    top: 0;
    left: 0;
    z-index: -10;
  }

  .screen {
    mask-origin: inherit;
    transform: rotate(var(--rotate)) skewX(var(--skewX)) skewY(var(--skewY)) translateY(var(--translateY))
      translateX(var(--translateX));
    -webkit-mask-repeat: no-repeat;
    mask-repeat: no-repeat;
    -webkit-mask-position: center;
    mask-position: center;
  }
</style>

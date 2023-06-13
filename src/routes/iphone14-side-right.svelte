<script lang="ts">
    export let skewY: any;
    export let translateY: any;
    export let translateX: any;
    // todo more vars
  
    export let screen: any;
    export let screenWidth: string;
    export let screenHeight: string;
  </script>
  
  <div class="container">
    <div class="screenMask">
      <img
        src={screen}
        alt="screen"
        class="screen"
        width={screenWidth}
        height={screenHeight}
        style="--skewY:{skewY};--translateY:{translateY};--translateX:{translateX};"
      />
    </div>
    <img src="/iphone14_side_right.png" alt="phone" class="phone" />
  </div>
  
  <style>
    .container {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 900px;
      height: 900px;
    }
  
    .screenMask {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 900px;
      height: 900px;
      -webkit-mask: url("/iphone14_side_right_mask.svg") no-repeat;
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
      transform: skewY(var(--skewY)) translateY(var(--translateY)) translateX(var(--translateX));
      -webkit-mask-repeat: no-repeat;
      mask-repeat: no-repeat;
      -webkit-mask-position: center;
      mask-position: center;
    }
  </style>
  
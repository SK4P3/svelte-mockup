<script lang="ts">
    export let screen: any;
    export let screenWidth: string;
</script>

<div class="container">
    <img src={screen} alt="screen" class="screen" width={screenWidth} />
    <img src="/iphone14_default.png" alt="phone" class="phone" />
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

    .phone {
        width: 900px;
        position: absolute;
        top: 0;
        left: 0;
        z-index: -10;
    }

    .screen {
        mask-origin: inherit;
        mask-image: url("iphone14_default_mask.svg");
        -webkit-mask-image: url("iphone14_default_mask.svg");
        -webkit-mask-repeat: no-repeat;
        mask-repeat: no-repeat;
        -webkit-mask-position: center;
        mask-position: center;
    }
</style>

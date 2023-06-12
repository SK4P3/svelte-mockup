<script lang="ts">
    import Iphone14Default from "./iphone14-default.svelte";
    import Iphone14SideRight from "./iphone14-side-right.svelte";
    import Iphone14SideLeft from "./iphone14-side-left.svelte";

    export let type: string = "default";
    export let screen: any;
    export let screenWidth: string;
</script>

{#if type === "default"}
    <Iphone14Default {screen} {screenWidth} />
{:else if type === "side-right"}
    <Iphone14SideRight {screen} {screenWidth} />
{:else if type === "side-left"}
    <Iphone14SideLeft {screen} {screenWidth} />
{/if}

<script lang="ts">
    import IPhone14 from "./IPhone14.svelte";
    import screenshot from "$lib/assets/screenshot.jpg";
    import screenshot2 from "$lib/assets/screenshot2.jpg";
</script>

<IPhone14 screen={screenshot} screenWidth="35%" type="side-left" />

<IPhone14 screen={screenshot} screenWidth="40%" type="side-right" />

<IPhone14 screen={screenshot} screenWidth="40%" />
<!-- <IPhone14 screen={screenshot2} screenWidth="47%" /> -->

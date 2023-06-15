<script lang="ts">
  import IPhone14 from "./IPhone14.svelte";
  import screenshot from "$lib/assets/screenshot.png";
  import screenshotWRLD from "$lib/assets/test.png";
</script>

<IPhone14 screen={screenshot} />

<IPhone14 screen={screenshot} type="side-right" />
<IPhone14 screen={screenshot} type="side-left" />

<IPhone14 screen={screenshot} type="hover-right" />
<IPhone14 screen={screenshot} type="hover-left" />

<IPhone14 screen={screenshot} type="front-and-back" />
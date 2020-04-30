<script>
  import Titlebar from "./components/Titlebar.svelte";
  import WindowBody from "./components/WindowBody.svelte";
</script>

<style>
  :global(body, html) {
    margin: 0;
    padding: 0;
  }
</style>

<div class="window" style="margin: 0; width: 100%; height: 100%; padding: 0;">
  <Titlebar title="Hello World!" />
  <WindowBody />
</div>

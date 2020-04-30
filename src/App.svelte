<script>
  import Titlebar from "./components/Titlebar.svelte";
  import WindowBody from "./components/WindowBody.svelte";

  import GroupBox from "./components/GroupBox.svelte";
  import GroupRow from "./components/GroupRow.svelte";
  import GroupRowStacked from "./components/GroupRowStacked.svelte";
</script>

<style>
  :global(body, html) {
    margin: 0;
    padding: 0;
  }
</style>

<div class="window" style="margin: 0; width: 100%; height: 100%; padding: 0;">
  <Titlebar title="Hello World!" />
  <WindowBody>
    <GroupBox>
      <GroupRow>
        <button>Click me!</button>
      </GroupRow>
      <GroupRowStacked>
        <input id="test" type="checkbox" />
        <label for="test">Test?</label>
      </GroupRowStacked>
    </GroupBox>
  </WindowBody>
</div>

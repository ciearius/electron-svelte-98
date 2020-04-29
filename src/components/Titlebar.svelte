<script>
  export let title;

  // Note: this is a workaround!
  // import remote from "electron"; // doesnt work.
  const { remote } = require("electron");
  const BrowserWindow = remote.BrowserWindow;

  function minimize() {
    getWindow().minimize();
  }

  function maximize() {
    getWindow().maximize();
  }

  function close() {
    getWindow().close();
  }

  function getWindow() {
    //  return remote.BrowserWindow.getFocusedWindow();
    return remote.getCurrentWindow();
  }
</script>

<style>
  .mover {
    -webkit-user-select: none;
    -webkit-app-region: drag;
  }
</style>

<svelte:head>
  <title>{title}</title>
</svelte:head>

<div class="title-bar mover">
  <div class="title-bar-text mover">{title}</div>
  <div class="title-bar-controls">
    <button on:click={minimize} aria-label="Minimize" />
    <button on:click={maximize} aria-label="Maximize" />
    <button on:click={close} aria-label="Close" />
  </div>
</div>

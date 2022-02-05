<script>
  import "carbon-components-svelte/css/all.css";

  import Preview from "./components/Preview.svelte";
  import Options from "./components/Options.svelte";

  let theme = "g100"; // "white" | "g10" | "g80" | "g90" | "g100"

  $: document.documentElement.setAttribute("theme", theme);
</script>

<main class="container mx-auto">
  <div class="row content-container">
    <div class="settings-area col-md-3">
      <Options />
    </div>
    <div class="preview-area col-md-6"><Preview /></div>
    <div class="preview-area col-md-3">s</div>
  </div>
</main>

<style>
  main {
    width: 100vw;
    height: 100vh;
  }

  .content-container {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .settings-area {
  }
  .preview-area {
  }
</style>

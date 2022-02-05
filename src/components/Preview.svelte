<script>
  import { previewTextStore } from "../stores/OptionsStore";
  let styles = {
    "fontsize-h1": "#f4ed2a",
    "fontsize-h2": "#FF5555",
    "fontsize-h3": "#AAAAAA",
    "fontsize-h4": "#f4ed2a",
    "fontsize-h5": "#FF5555",
    "fontsize-h6": "#AAAAAA",
    "fontsize-blockquote": "#f4ed2a",
    "fontsize-body": "#FF5555",
    "fontsize-caption": "#AAAAAA",
    "fontsize-endnote": "#f4ed2a",
    "fontsize-footnote": "#FF5555",
  };

  $: cssVarStyles = Object.entries(styles)
    .map(([key, value]) => `--${key}:${value}`)
    .join(";");

  let previewText = "";

  previewTextStore.subscribe((data) => {
    previewText = data;
  });
</script>

<div style={cssVarStyles} class="preview-container">
  <div class="preview-item-container">
    <label for="h1">H1</label>
    <h1 id="h1" class="h1-preview">{previewText}</h1>
  </div>
  <div class="preview-item-container">
    <label for="h2">H2</label>
    <h2 id="h2" class="h2-preview">{previewText}</h2>
  </div>
  <div class="preview-item-container">
    <label for="h3">H3</label>
    <h3 id="h3" class="h3-preview">{previewText}</h3>
  </div>
  <div class="preview-item-container">
    <label for="h4">H4</label>
    <h4 id="h4" class="h4-preview">{previewText}</h4>
  </div>
  <div class="preview-item-container">
    <label for="h5">H5</label>
    <h5 id="h5" class="h5-preview">{previewText}</h5>
  </div>
  <div class="preview-item-container">
    <label for="h6">H6</label>
    <h6 id="h6" class="h6-preview">{previewText}</h6>
  </div>
  <div class="preview-item-container">
    <label for="blockquote">Blockquote</label>
    <p id="blockquote" class="blockquote-preview">{previewText}</p>
  </div>
  <div class="preview-item-container">
    <label for="body">Body</label>
    <p id="body" class="body-preview">{previewText}</p>
  </div>
  <div class="preview-item-container">
    <label for="caption">Caption</label>
    <p id="caption" class="caption-preview">{previewText}</p>
  </div>
  <div class="preview-item-container">
    <label for="endnote">Endnote</label>
    <p id="endnote" class="endnote-preview">{previewText}</p>
  </div>
  <div class="preview-item-container">
    <label for="footnote">Footnote</label>
    <p id="footnote" class="footnote-preview">{previewText}</p>
  </div>
</div>

<style>
  .preview-container {
    width: 100%;
  }
  .preview-item-container {
    margin-bottom: 20px;
    padding-bottom: 10px;
    border-bottom: 1px solid white;
  }

  .h1-preview {
  }
  .h2-preview {
  }
  .h3-preview {
  }
  .h4-preview {
  }
  .h5-preview {
  }
  .h6-preview {
  }
  .blockquote-preview {
  }
  .body-preview {
  }
  .caption-preview {
  }
  .endnote-preview {
  }
  .footnote-preview {
  }
</style>

<script>
  import { previewTextStore } from "../src/stores/OptionsStore";
  import { afterUpdate } from "svelte";

  import {
    NumberInput,
    Select,
    SelectItem,
    TextInput,
    Button,
  } from "carbon-components-svelte";

  let previewTextValue = "Example Text";

  afterUpdate(() => {
    previewTextStore.set(previewTextValue);
  });
</script>

<div class="input-area-margin">
  <NumberInput invalid={false} hideSteppers label="Base Size" value={16} />
</div>
<div class="input-area-margin">
  <Select labelText="Scale" selected="g10">
    <SelectItem value="minor-second" text="1.067 Minor Second" />
    <SelectItem value="major-second" text="1.125 Major Second" />
    <SelectItem value="minor-third" text="1.200 Minor Third" />
    <SelectItem value="major-third" text="1.250 Major Third" />
    <SelectItem value="perfect-fourth" text="1.333 Perfect Fourth" />
    <SelectItem value="augmented-fourth" text="1.414 Augmented Fourth" />
    <SelectItem value="perfect-fifth" text="1.500 Perfect Fifth" />
    <SelectItem value="golden-ratio" text="1.618 Golden Ratio" />
    <SelectItem value="custom" text="Custom..." />
  </Select>
</div>
<div class="input-area-margin">
  <Select labelText="Google Fonts" selected="g10">
    <SelectItem value="white" text="White" />
    <SelectItem value="g10" text="Gray 10" />
    <SelectItem value="g80" text="Gray 80" />
    <SelectItem value="g90" text="Gray 90" />
    <SelectItem value="g100" text="Gray 100" />
  </Select>
</div>
<div class="input-area-margin">
  <Select labelText="Weight" selected="g10">
    <SelectItem value="white" text="White" />
    <SelectItem value="g10" text="Gray 10" />
    <SelectItem value="g80" text="Gray 80" />
    <SelectItem value="g90" text="Gray 90" />
    <SelectItem value="g100" text="Gray 100" />
  </Select>
</div>
<div class="input-area-margin">
  <TextInput bind:value={previewTextValue} labelText="Preview Text" />
</div>
<div class="input-area-margin">
  <Button kind="danger-ghost">Reset All</Button>
</div>

<style>
</style>

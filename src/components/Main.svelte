<script>
  import { derived } from "svelte/store";
</script>

<div class="Main">
  <div class="Main-container">
    <slot />
  </div>
</div>

<style>
  .Main-container {
    display: flex;
    justify-content: center;
  }
</style>

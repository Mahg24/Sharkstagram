<script>
  import Card from "./Card.svelte";
  export let icons;
</script>

<div class="Timeline">
  <div class="Timeline-container">
    <Card {icons} />
  </div>
</div>

<style>
  .Timeline {
    width: 100%;
    max-width: 1100px;
  }
</style>

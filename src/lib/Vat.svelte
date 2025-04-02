<script>
  import { hasVat } from './state.svelte';

  const toggle = () => {
    $hasVat = !$hasVat;
  }
</script>

<div>
  <button class="button" on:click={toggle}>Toggle Vat: {$hasVat ? "ON" : "OFF"}</button>
</div>

<style>
  .button{
    border-color: blue;
  }
</style>

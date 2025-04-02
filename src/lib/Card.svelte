<script>
  import { hasVat } from './state.svelte';
  let { title, description, price } = $props();
</script>

<div class="card">
    <h2>{title}</h2>
    <p>{description}</p>
    <p>${$hasVat ? price * 1.2 : price}</p>
</div>

<style>
    .card {
        border: 1px solid tomato;
        width: 500px;
        
    }
    h2 {
        font-size: 30px;
        font-weight: var(--font-weight-8);
    }
    p {
        font-weight: var(--font-weight-4);
    }
</style>
  
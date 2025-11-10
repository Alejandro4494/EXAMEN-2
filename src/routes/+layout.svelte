<script>
  import Nav from '$lib/components/Nav.svelte';
</script>

<Nav />
<slot />

<style>
  :global(body) { margin:0; font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; background:#f3f4f6; color:#0f172a; }
  main { padding:1rem; max-width:900px; margin: 0 auto; }
</style>
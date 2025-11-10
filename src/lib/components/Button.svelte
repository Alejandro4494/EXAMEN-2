<script>
  export let type = 'button';
  export let variant = 'primary';
</script>

<button class={"btn " + variant} type={type}>
  <slot />
</button>

<style>
  .btn { padding: .45rem .75rem; border-radius:6px; border: none; cursor:pointer; font-weight:600; }
  .primary { background:#2563eb; color:white; }
  .secondary { background:#e5e7eb; color:#0f172a; }
</style>
<script>
  export let title = '';
  export let excerpt = '';
  export let href = '#';
</script>

<article class="card">
  <h3><a class="link" href={href}>{title}</a></h3>
  <p>{excerpt}</p>
  <slot />
</article>

<style>
  .card {
    border: 1px solid #e6e7ea;
    padding: 0.9rem;
    border-radius: 8px;
    background: #fff;
    box-shadow: 0 1px 2px rgba(16,24,40,0.03);
  }
  h3 { margin: 0 0 0.5rem 0; font-size: 1.05rem; }
  p { margin: 0; color: #374151; font-size: 0.95rem; }
  .link { color: #0f172a; text-decoration: none; }
  .link:hover { text-decoration: underline; }
</style>
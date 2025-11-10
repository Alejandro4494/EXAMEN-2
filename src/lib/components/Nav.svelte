<script>
  // componente de navegacion simple
</script>

<header class="nav">
  <div class="brand"><a href="/">Evaluacion SvelteKit</a></div>
  <nav class="links">
    <a href="/">Home</a>
    <a href="/pagina-fija">Pagina fija</a>
  </nav>
</header>

<style>
  .nav {
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:0.75rem 1rem;
    background:#f8fafc;
    border-bottom:1px solid #e6e7ea;
  }
  .brand a { font-weight:700; color:#0f172a; text-decoration:none; }
  .links a { margin-left:1rem; color:#0f172a; text-decoration:none; }
  .links a:hover { text-decoration:underline; }
</style>
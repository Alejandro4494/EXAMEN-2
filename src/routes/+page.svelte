<script>
  import Card from '$lib/components/Card.svelte';

  const posts = [
    { slug: 'hola-mundo', title: 'Hola Mundo', excerpt: 'Primer post de ejemplo' },
    { slug: 'sveltekit-intro', title: 'Intro a SvelteKit', excerpt: 'Guia rapida para empezar' },
    { slug: 'evaluacion-guia', title: 'Guia de la evaluacion', excerpt: 'Explicacion breve del proyecto entregable' }
  ];
</script>

<main>
  <h1>Inicio</h1>
  <p>Mini blog de ejemplo para la evaluacion. Haz clic en una tarjeta para ver la ruta dinamica.</p>

  <section class="grid">
    {#each posts as p}
      <Card title={p.title} excerpt={p.excerpt} href={`/${p.slug}`} />
    {/each}
  </section>
</main>

<style>
  h1 { margin-top:0; }
  .grid { display:grid; gap:1rem; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); margin-top:1rem; }
</style>
<script>
  import { page } from '$app/stores';
  import { onDestroy } from 'svelte';

  // Datos en memoria para la evaluacion
  const POSTS = {
    'hola-mundo': { title: 'Hola Mundo', body: 'Contenido del post Hola Mundo.' },
    'sveltekit-intro': { title: 'Intro a SvelteKit', body: 'Contenido de la guia SvelteKit.' },
    'evaluacion-guia': { title: 'Guia de la evaluacion', body: 'Detalles y checklist para la entrega.' }
  };

  let slug;
  let post;

  const unsubscribe = page.subscribe(p => {
    slug = p.params.slug;
    post = POSTS[slug] ?? { title: 'No encontrado', body: 'No existe contenido para este slug.' };
  });

  onDestroy(() => unsubscribe());
</script>

<main>
  <h1>{post.title}</h1>
  <p>{post.body}</p>
</main>

<style>
  main { padding-bottom:2rem; }
  h1 { margin-top:0; }
</style>
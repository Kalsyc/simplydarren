<script lang="ts">
  export let name: string;
  import { Router } from '@roxi/routify';
  import { routes } from '../.routify/routes';
</script>

<main>
  <Router {routes} />
</main>

<style>
  main {
    min-width: inherit;
    min-height: inherit;
    width: 100%;
    height: 100%;
  }
</style>

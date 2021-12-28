<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
  import FooterComponent from '../../components/FooterComponent.svelte';
  import { url, metatags } from '@roxi/routify';

  metatags.title = 'Projects';
</script>

<main>
  <HeaderComponent />
  <div class="project-main-div">
    <span class="project-title-div">Coming Soon :)</span>
    <a class="cullinary-link" href={$url('/projects/cull1')}>Click here to play CULLinary</a>
    <a class="cullinary-link" href={$url('/projects/cull2')}>Click here to play CULLinary2</a>
  </div>
  <FooterComponent />
</main>

<style>
  .project-main-div {
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 1em 0;
    min-height: 100vh;
  }

  .project-title-div {
    font-size: 1.5rem;
    font-weight: 500;
    margin: 1em 0;
  }

  .cullinary-link {
    margin: 1em 0;
    color: black;
    text-decoration: none;
  }

  .cullinary-link:hover {
    text-decoration: underline;
    opacity: 0.5;
    cursor: pointer;
  }
</style>

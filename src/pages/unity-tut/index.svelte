<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
  import FooterComponent from '../../components/FooterComponent.svelte';
  import { metatags, url } from '@roxi/routify';

  metatags.title = 'Simply Darren | Unity Tutorials';
</script>

<main>
  <HeaderComponent />
  <div class="blog-main-div">
    <span class="blog-title-div">For CS4240 S2 AY2122</span>
    <span class="blog-title-div">Useful Guides</span>
  </div>
  <FooterComponent />
</main>

<style>
  .blog-main-div {
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 1em 0;
    min-height: 100vh;
  }

  .blog-title-div {
    font-size: 1.5rem;
    font-weight: 500;
    margin: 1em 0;
  }
</style>

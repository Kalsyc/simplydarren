<script lang="ts">
  import HeaderComponent from '../components/HeaderComponent.svelte';
  import FooterComponent from '../components/FooterComponent.svelte';
  import { metatags } from '@roxi/routify';

  metatags.title = 'About';
</script>

<main>
  <HeaderComponent />
  <div class="about-main-div">
    <span class="about-title-div">Coming Soon :)</span>
  </div>
  <FooterComponent />
</main>

<style>
  .about-main-div {
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 1em 0;
    min-height: 100vh;
  }

  .about-title-div {
    font-size: 1.5rem;
    font-weight: 500;
    margin: 1em 0;
  }
</style>

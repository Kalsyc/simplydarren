<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
  import FooterComponent from '../../components/FooterComponent.svelte';
  import { metatags, params } from '@roxi/routify';
  import { onMount } from 'svelte';

  let mdDesc;
  let projectName: string = $params.project;
  metatags.title = 'Simply Darren | ' + projectName;

  const importMarkdown = async () => {
    return await import(`../../markdown/PetSaver.md`);
  };

  onMount(() => {
    importMarkdown().then((res) => {
      mdDesc = res.default;
    });
  });
</script>

<main>
  <HeaderComponent />
  <div class="main-div">
    <svelte:component this={mdDesc} />
  </div>
  <FooterComponent />
</main>

<style>
  .main-div {
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 1em 0;
    min-height: 100vh;
  }
</style>

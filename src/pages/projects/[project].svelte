<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
  import FooterComponent from '../../components/FooterComponent.svelte';
  import { metatags, params } from '@roxi/routify';
  import { onMount } from 'svelte';

  let mdDesc;
  let projectName: string = $params.project;
  metatags.title = 'Simply Darren | ' + (projectName === undefined ? 'Error' : projectName.replaceAll('%20', ' '));

  const importMarkdown = async () => {
    switch (projectName) {
      case 'PetSaver':
        return await import(`../../markdown/PetSaver.md`);
      case 'SafeSpace':
        return await import(`../../markdown/SafeSpace.md`);
      case 'ProjectKampong':
        return await import(`../../markdown/ProjectKampong.md`);
      case 'DigitalKampung':
        return await import(`../../markdown/DigitalKampung.md`);
      case 'CULLinary':
        return await import(`../../markdown/CULLinary.md`);
      case 'CULLinary2':
        return await import(`../../markdown/CULLinary2.md`);
      case 'Xpire':
        return await import(`../../markdown/Xpire.md`);
      case 'CanMakan':
        return await import(`../../markdown/CanMakan.md`);
      case 'Yobu':
        return await import(`../../markdown/Yobu.md`);
      case 'SayNoToUILibraries':
        return await import(`../../markdown/SayNoToUILibraries.md`);
      default:
        return await import(`../../markdown/Error.md`);
    }
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
    <div class="markdown-component">
      <svelte:component this={mdDesc} />
    </div>
  </div>
  <FooterComponent />
</main>

<style>
  .main-div {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 1em 0;
    min-height: 100vh;
  }

  .markdown-component {
    width: 50%;
  }
</style>

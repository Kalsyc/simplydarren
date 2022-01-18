<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
  import FooterComponent from '../../components/FooterComponent.svelte';
  import { metatags, params } from '@roxi/routify';
  import { onMount } from 'svelte';

  let mdDesc;
  let labTitle: string = $params.labTitle;
  metatags.title = 'Simply Darren | ' + (labTitle === undefined ? 'Error' : labTitle.replaceAll('%20', ' '));

  const importMarkdown = async () => {
    switch (labTitle) {
      case 'Setup':
        return await import(`../../markdown/cs4240/setup.md`);
      case 'Lab 1':
        return await import(`../../markdown/cs4240/lab1.md`);
      case 'VSCode Setup':
        return await import(`../../markdown/cs4240/vscode-setup.md`);
      default:
        return await import(`../../markdown/cs4240/Error.md`);
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

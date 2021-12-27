<script lang="ts">
  import { goto, url } from '@roxi/routify';

  const goToHome = (): void => {
    $goto('/');
  };
</script>

<div class="header-background-div">
  <div class="header-items-div">
    <span class="header-title-span" on:click={() => goToHome()}>SIMPLY DARREN</span>
    <div class="header-links-div">
      <a class="header-link" href={$url('/about')}>About</a>
      <a class="header-link" href={$url('/projects')}>Projects</a>
      <a class="header-link" href="https://www.linkedin.com/in/kalsyc/"><img class="header-img-link" alt="" src="/img/LI-In-Bug.png" /></a>
      <a class="header-link" href="https://github.com/Kalsyc"><img class="header-img-link" alt="" src="/img/GitHub-Mark-64px.png" /></a>
    </div>
  </div>
</div>

<style>
  .header-background-div {
    background-color: #efe2ba;
    height: 60px;
    min-height: inherit;
    min-width: inherit;
    width: 100vw;
  }

  .header-items-div {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: inherit;
    min-height: inherit;
    padding: 0 1em;
  }

  .header-title-span {
    font-size: 2rem;
    font-weight: 700;
    padding: 0 0.5em;
  }

  .header-title-span:hover {
    cursor: pointer;
  }

  .header-links-div {
    font-size: 1.25rem;
    font-weight: 600;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }

  .header-img-link {
    object-fit: contain;
    aspect-ratio: 1;
    height: 32px;
    width: 32px;
    display: block;
  }

  .header-img-link:hover {
    cursor: pointer;
    opacity: 0.5;
  }

  .header-link {
    margin: 0 5px;
    color: black;
    text-decoration: none;
  }

  .header-link:hover {
    text-decoration: underline;
    opacity: 0.5;
    cursor: pointer;
  }

  @media only screen and (max-width: 600px) {
    .header-links-div {
      display: none;
    }
  }
</style>

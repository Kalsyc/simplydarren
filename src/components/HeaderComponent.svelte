<script lang="ts">
  import { goto, url } from '@roxi/routify';

  const goToAbout = (): void => {
    $goto('/home');
  };
</script>

<div class="header-background-div">
  <div class="header-items-div">
    <span class="header-title-span">SIMPLY DARREN</span>
    <div class="header-links-div">
      <a class="header-link" href={$url('/about')}>About</a>
      <a class="header-link" href={$url('/projects')}>Projects</a>
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
  }

  .header-title-span {
    font-size: 2rem;
    font-weight: 700;
    padding: 0 0.5em;
  }

  .header-links-div {
    font-size: 1.25rem;
    font-weight: 600;
    display: grid;
    grid-auto-flow: column;
    align-self: center;
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

  @media only screen and (max-width: 500px) {
    .header-links-div {
      display: none;
    }
  }
</style>

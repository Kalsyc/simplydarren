<script lang="ts">
  import { goto, url } from '@roxi/routify';

  let isNavOpen: boolean = false;

  const goToHome = (): void => {
    $goto('/');
  };

  const toggleNav = (): void => {
    const dropdownDiv: HTMLElement = document.getElementById('header-dropdown-div');
    dropdownDiv.style.width = isNavOpen ? '150px' : '0px';
    isNavOpen = !isNavOpen;
  };
</script>

<div class="header-background-div">
  <div class="header-items-div">
    <span class="header-title-span" on:click={() => goToHome()}>SIMPLY DARREN</span>
    <a class="header-title-span-res" href={$url('/')}><img class="header-title-img-res" alt="" src="/img/Simply Darren Transparent.png" /></a>
    <div class="header-links-div">
      <a class="header-link" href={$url('/about')}>About</a>
      <a class="header-link" href={$url('/blog')}>Blog</a>
      <a class="header-link" href={$url('/projects')}>Projects</a>
      <a class="header-link" href="https://www.linkedin.com/in/kalsyc/"><img class="header-img-link" alt="" src="/img/LI-In-Bug.png" /></a>
      <a class="header-link" href="https://github.com/Kalsyc"><img class="header-img-link" alt="" src="/img/GitHub-Mark-64px.png" /></a>
    </div>
    <div class="header-links-nav-res">
      <img class="header-dropdown-img-res" alt="" src="/img/outline_menu_black_36dp.png" on:click={() => toggleNav()} />
      <div id="header-dropdown-div" class="header-dropdown-div">
        <a class="header-link-res" href={$url('/about')}>About</a>
        <a class="header-link-res" href={$url('/blog')}>Blog</a>
        <a class="header-link-res" href={$url('/projects')}>Projects</a>
        <a class="header-link-res" href="https://github.com/Kalsyc">GitHub</a>
        <a class="header-link-res" href="https://www.linkedin.com/in/kalsyc/">LinkedIn</a>
      </div>
    </div>
  </div>
</div>

<style>
  .header-background-div {
    background-color: #efe2ba;
    height: 60px;
    min-height: inherit;
    min-width: inherit;
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

  .header-title-span-res {
    display: none;
  }

  .header-title-img-res {
    object-fit: contain;
    aspect-ratio: 1;
    height: 60px;
    width: 60px;
    display: block;
  }

  .header-title-span {
    font-size: 2rem;
    font-weight: 700;
    padding: 0 0.5em;
    color: #e87121;
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

  .header-links-nav-res {
    display: none;
    height: 60px;
    width: 60px;
    text-align: center;
  }

  .header-dropdown-img-res {
    height: inherit;
    width: inherit;
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
    margin: 0 0.35em;
    color: #e87121;
    text-decoration: none;
  }

  .header-link:hover {
    text-decoration: underline;
    opacity: 0.5;
    cursor: pointer;
  }

  .header-link-res {
    text-decoration: none;
    color: #e87121;
    margin: 0.4em;
  }

  .header-dropdown-div {
    height: 100%;
    width: 0;
    position: fixed;
    z-index: 1;
    top: 59px;
    right: 0;
    background-color: #efe2ba;
    overflow-x: hidden;
    padding-top: 30px;
    transition: 0.5s;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  /* Media queries */

  @media only screen and (max-width: 600px) {
    .header-links-div,
    .header-title-span {
      display: none;
    }

    .header-title-span-res {
      display: block;
    }

    .header-links-nav-res {
      display: inline-block;
    }
  }
</style>

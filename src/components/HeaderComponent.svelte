<script lang="ts">
  import { goto, url } from '@roxi/routify';

  const goToHome = (): void => {
    $goto('/');
  };

  const toggleNav = (isNavOpen: boolean): void => {
    const dropdownDiv: HTMLElement = document.getElementById('header-dropdown-div');
    dropdownDiv.style.width = isNavOpen ? '150px' : '0px';
  };
</script>

<div class="header-background-div">
  <div class="header-items-div">
    <a class="title-link" href={$url('/')}><span class="header-title-span">SIMPLY DARREN</span></a>
    <a class="header-title-span-res" href={$url('/')}><img class="header-title-img-res" alt="" src="/img/Simply Darren Transparent.png" /></a>
    <div class="header-links-div">
      <a class="header-link" href={$url('/about')}>About</a>
      <a class="header-link" href={$url('/blog')}>Blog</a>
      <a class="header-link" href={$url('/projects')}>Projects</a>
      <a class="header-link" href="https://www.linkedin.com/in/kalsyc/"><img class="header-img-link" alt="" src="/img/LI-In-Bug.png" /></a>
      <a class="header-link" href="https://github.com/Kalsyc"><img class="header-img-link" alt="" src="/img/GitHub-Mark-64px.png" /></a>
    </div>
    <div class="header-links-nav-res">
      <img class="header-dropdown-img-res" alt="" src="/img/outline_menu_black_36dp.png" on:click={() => toggleNav(true)} />
      <div id="header-dropdown-div" class="header-dropdown-div">
        <img class="header-dropdown-close-res" alt="" src="/img/outline_arrow_forward_black_36dp.png" on:click={() => toggleNav(false)} />
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
    height: 50px;
    width: 50px;
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

  .title-link {
    text-decoration: none;
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
    height: 50px;
    width: 50px;
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

  .header-dropdown-close-res {
    height: 50px;
    width: 50px;
  }

  .header-dropdown-div {
    height: 100%;
    width: 0;
    position: fixed;
    top: 0;
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

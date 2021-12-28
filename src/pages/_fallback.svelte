<script lang="ts">
  import { url } from '@roxi/routify';
  import { metatags } from '@roxi/routify';

  metatags.title = 'Error! Not found';
</script>

<main>
  <div class="main-div">
    <span class="title-span">Error 404</span>
    <span> This page doesn't exist at the moment :(</span>
    <a class="click-span" href={$url('/')}>Click here to go back.</a>
  </div>
</main>

<style>
  main {
    height: 100vh;
    background-color: #efe2ba;
  }

  .main-div {
    text-align: center;
    height: inherit;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .title-span {
    font-size: 5rem;
    color: black;
  }

  .click-span {
    text-decoration: underline;
    color: black;
  }

  .click-span:hover {
    opacity: 0.5;
    cursor: pointer;
  }
</style>

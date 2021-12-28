<script lang="ts">
  import { goto, url } from '@roxi/routify';
</script>

<div class="footer-background-div">
  <div class="footer-items-div">
    <div class="footer-links-div">
      <a class="footer-link" href={$url('/about')}>About</a>
      <a class="footer-link" href={$url('/blog')}>Blog</a>
      <a class="footer-link" href={$url('/projects')}>Projects</a>
      <a class="footer-link" href="https://github.com/Kalsyc">GitHub</a>
      <a class="footer-link" href="https://www.linkedin.com/in/kalsyc/">LinkedIn</a>
    </div>
    <span class="footer-copyright">(c) Sim Jun Yuen, Darren 2021</span>
  </div>
</div>

<style>
  .footer-background-div {
    background-color: #efe2ba;
    height: 100px;
    min-height: inherit;
    min-width: inherit;
  }

  .footer-items-div {
    height: inherit;
    width: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .footer-links-div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  .footer-link {
    font-size: 1.1rem;
    font-weight: 700;
    margin: 0.2em;
    color: #e87121;
    text-decoration: none;
  }

  .footer-link:hover {
    text-decoration: underline;
    opacity: 0.5;
    cursor: pointer;
  }

  .footer-copyright {
    margin: 0.2em;
    color: #2c3e50;
  }
</style>

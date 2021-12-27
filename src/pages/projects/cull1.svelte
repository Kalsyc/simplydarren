<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
</script>

<main>
  <HeaderComponent />
  <div class="cullinary-game-div">
    <iframe
      src="https://simplydarren-test.s3.ap-southeast-1.amazonaws.com/CULLinary_WebGL_Build_Prod/index.html"
      name="CULLinary"
      scrolling="no"
      frameborder="1"
      height="760px"
      width="1280px"
      title="CULLinary"
      class="cullinary-iframe"
    />
  </div>
</main>

<style>
  .cullinary-game-div {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 10px;
    height: 760px;
  }

  .cullinary-iframe {
    border: 0px #000000 none;
    height: 760px;
    width: 1280px;
  }
</style>

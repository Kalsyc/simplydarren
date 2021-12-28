<script lang="ts">
  import HeaderComponent from '../components/HeaderComponent.svelte';
  import { metatags, url, goto } from '@roxi/routify';
  import FooterComponent from '../components/FooterComponent.svelte';

  metatags.title = 'Simply Darren';

  const goToAbout = (): void => {
    $goto('/about');
  };

  const goToProjects = (): void => {
    $goto('/projects');
  };

  const sendEmail = (): void => {
    window.location.assign('mailto:kalsycofficial@gmail.com');
  };

  const goToResume = (): void => {
    window.location.assign('https://kalsycdotcom.s3.ap-southeast-1.amazonaws.com/Sim+Jun+Yuen%2C+Darren+Resume+(28+Dec+2021).pdf');
  };
</script>

<HeaderComponent />
<div class="main-body-div">
  <div class="main-intro-div">
    <span class="intro-item intro-name-span">Darren Sim</span>
    <span class="intro-item intro-title-span">Software Engineer & UI/UX Designer</span>
    <span class="intro-item intro-based-span">Based in Singapore</span>
  </div>
  <div class="main-brief-div">
    <div class="main-img-div"><img class="main-img" alt="" src="/img/face.jpg" /></div>
    <div class="main-short-div">
      Hey there! I'm Darren Sim, a Final Year Computer Science Major at National University of Singapore (NUS).
      <br /><br />
      My main areas of expertise are Web Development and UI/UX Design. I sometimes teach and develop games on the side :3 Feel free to browse through my
      website to find out more!
    </div>
  </div>
  <div class="main-buttons-div">
    <button class="main-button" on:click={() => goToAbout()}>About Me</button>
    <button class="main-button" on:click={() => goToResume()}>Resume</button>
    <button class="main-button" on:click={() => sendEmail()}>Contact Me</button>
    <button class="main-button" on:click={() => goToProjects()}>My Projects</button>
  </div>
</div>
<FooterComponent />

<style>
  .main-body-div {
    min-height: 100vh;
    -webkit-animation: fadein 2s;
    -moz-animation: fadein 2s;
    -ms-animation: fadein 2s;
    -o-animation: fadein 2s;
    animation: fadein 2s;
  }

  .main-intro-div {
    color: #2c3e50;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2em 0 0 0;
    text-align: center;
  }

  .intro-item {
    margin: 5px 0;
  }

  .intro-name-span {
    font-size: 4rem;
    font-weight: 700;
  }

  .intro-title-span {
    font-size: 2rem;
    font-weight: 500;
  }

  .intro-based-span {
    font-size: 1.25rem;
    font-weight: 400;
  }

  .main-brief-div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin: 1em 0;
  }

  .main-img-div {
    margin: 0.5em 3em;
  }

  .main-img {
    border-radius: 50%;
    aspect-ratio: 1;
    height: 200px;
    width: 200px;
  }

  .main-short-div {
    font-size: 1.25rem;
    font-weight: 400;
    margin: 0 1em;
  }

  .main-buttons-div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 3em 1em;
  }

  .main-button {
    margin: 2em 1em;
    width: 175px;
    height: 50px;
    color: #2c3e50;
    border-radius: 10px;
    font-weight: 700;
    font-size: 1.1rem;
    font-family: 'Titillium Web';
    background-color: #fff;
    border-color: #2c3e50;
    transition: 0.2s ease-in;
    -o-transition: 0.2s ease-in;
    -ms-transition: 0.2s ease-in;
    -moz-transition: 0.2s ease-in;
    -webkit-transition: 0.2s ease-in;
  }

  .main-button:hover {
    background-color: #efe2ba;
    color: #e87121;
    cursor: pointer;
  }

  @media only screen and (max-width: 600px) {
    .main-brief-div {
      flex-direction: column;
    }

    .main-buttons-div {
      flex-direction: column;
    }

    .main-button {
      background-color: #efe2ba;
      color: #e87121;
    }
  }

  @keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  /* Firefox < 16 */
  @-moz-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  /* Safari, Chrome and Opera > 12.1 */
  @-webkit-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  /* Internet Explorer */
  @-ms-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  /* Opera < 12.1 */
  @-o-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
</style>

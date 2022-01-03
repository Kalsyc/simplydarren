<script lang="ts">
  import HeaderComponent from '../../components/HeaderComponent.svelte';
  import FooterComponent from '../../components/FooterComponent.svelte';
  import { url, metatags } from '@roxi/routify';

  metatags.title = 'Simply Darren | Projects';
</script>

<main>
  <HeaderComponent />
  <div class="project-main-div">
    <span class="project-title-div">My Projects</span>
    <div class="projects-completed">
      <span class="completed-title">Completed Projects</span>
      <div class="completed-grid">
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'PetSaver' })}>
            <img class="completed-img" alt="" src="/img/petsaver-img.jpeg" />
            <div class="completed-overlay">
              <div class="completed-text">
                PetSaver
                <br />
                Personal Savings App for UX Design Student Project
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'ProjectKampong' })}>
            <img class="completed-img" alt="" src="/img/kampong-img.png" />
            <div class="completed-overlay">
              <div class="completed-text">
                Project Kampong
                <br />
                An online collaborative platform for the Social Sector
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'DigitalKampung' })}>
            <img class="completed-img" alt="" src="/img/digitalkampung-img.png" />
            <div class="completed-overlay">
              <div class="completed-text">
                Digital Kampung
                <br />
                Search, Review and Rate Hawker stalls across Singapore!
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/cull1')}>
            <img class="completed-img" alt="" src="/img/cullinary-gif.gif" />
            <div class="completed-overlay">
              <div class="completed-text">
                CULLinary
                <br />
                Student Game Project, 1st Place at 18th iSTePS
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/cull2')}>
            <img class="completed-img" alt="" src="/img/cullinary2-gif.gif" />
            <div class="completed-overlay">
              <div class="completed-text">
                CULLinary2
                <br />
                Student Game Project, 1st Place at 19th iSTePS
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'SafeSpace' })}>
            <img class="completed-img" alt="" src="/img/safespace-img.png" />
            <div class="completed-overlay">
              <div class="completed-text">
                SafeSpace
                <br />
                VR Mental Health Simulator and Meditation Guide
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
    <!--
    <div class="projects-ongoing">
      <span class="ongoing-title">Ongoing Projects</span>
    </div>
    -->
  </div>
  <FooterComponent />
</main>

<style>
  .project-main-div {
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 1em 0;
    min-height: 100vh;
  }

  .completed-grid {
    padding: 1em 0;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }

  .completed-cell {
    margin: 0.5em;
    position: relative;
  }

  .completed-cell:hover {
    cursor: pointer;
  }

  .completed-cell:hover .completed-overlay {
    opacity: 1;
  }

  .completed-img {
    display: block;
    height: 225px;
    width: 425px;
    aspect-ratio: 1;
    object-fit: cover;
    border-radius: 1em;
  }

  .completed-overlay {
    border-radius: 1em;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: 0.3s ease-in;
    background-color: rgba(0, 0, 0, 0.6);
  }

  .completed-text {
    width: auto;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-weight: 700;
    font-size: 1.25rem;
  }

  .completed-title,
  .ongoing-title {
    font-weight: 700;
    font-size: 1.5rem;
    color: #e87121;
    text-decoration: underline;
  }

  .projects-completed,
  .projects-ongoing {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    margin: 1em 10%;
  }

  .project-title-div {
    color: #e87121;
    font-weight: 700;
    font-size: 2rem;
    font-weight: 500;
    margin: 5px 0;
  }
</style>

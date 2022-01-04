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
              <div class="completed-tag">UX/UI Design</div>
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
              <div class="completed-tag">Web Dev</div>
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
              <div class="completed-tag">Web Dev</div>
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
              <div class="completed-tag">Game Dev</div>
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
              <div class="completed-tag">Game Dev</div>
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
              <div class="completed-tag">Virtual Reality</div>
              <div class="completed-text">
                SafeSpace
                <br />
                VR Mental Health Simulator and Meditation Guide
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'Xpire' })}>
            <img class="completed-img" alt="" src="/img/xpire-img.png" />
            <div class="completed-overlay">
              <div class="completed-tag">App Dev</div>
              <div class="completed-text">
                Xpire
                <br />
                Desktop Expiry Date Tracker Application written in Java
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'CanMakan' })}>
            <img class="completed-img" alt="" src="/img/canmakan.jpg" />
            <div class="completed-overlay">
              <div class="completed-tag">Web Dev</div>
              <div class="completed-text">
                CanMakan
                <br />
                Website that checks dine-in rules for vaccinated people
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>

    <div class="projects-ongoing">
      <span class="ongoing-title">Ongoing Projects</span>
      <div class="completed-grid">
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'Yobu' })}>
            <img class="completed-img" alt="" src="/img/yobu.jpg" />
            <div class="completed-overlay">
              <div class="completed-tag">Web Dev</div>
              <div class="completed-text">
                Yobu
                <br />
                Social Gaming Platform - The newest way to connect
              </div>
            </div>
          </a>
        </div>
        <div class="completed-cell">
          <a href={$url('/projects/:project', { project: 'SayNoToUILibraries' })}>
            <img class="completed-img" alt="" src="/img/saynotouilibraries.jpg" />
            <div class="completed-overlay">
              <div class="completed-tag">Web Dev</div>
              <div class="completed-text">
                SayNoToUILibraries
                <br />
                Houses all my Frontend Components and UI Elements
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
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
    width: 400px;
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

  .completed-tag {
    position: absolute;
    top: 3%;
    left: 3%;
    color: white;
    font-weight: 700;
    border-radius: 10px;
    background-color: #e87121;
    padding: 0 0.5em;
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
    padding: 0 1em;
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
    align-items: center;
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

  @media screen and (max-width: 1400px) {
    .completed-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media screen and (max-width: 900px) {
    .completed-grid {
      grid-template-columns: repeat(1, 1fr);
    }

    .completed-overlay {
      top: 50%;
      height: 50%;
      opacity: 1;
    }

    .completed-text {
      text-align: left;
      font-size: 1rem;
      justify-content: flex-start;
    }
  }

  @media screen and (max-width: 600px) {
    .completed-img {
      height: 40vw;
      width: 80vw;
    }
    .completed-tag {
      position: relative;
      text-align: left;
      max-width: 35%;
      text-overflow: ellipsis;
      overflow: hidden;
      white-space: nowrap;
    }
  }

  @media screen and (max-width: 400px) {
    .completed-text,
    .completed-tag {
      font-size: 0.75rem;
    }
  }
</style>

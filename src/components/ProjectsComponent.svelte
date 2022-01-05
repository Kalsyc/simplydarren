<script lang="ts">
  import { url } from '@roxi/routify';

  /*
  import { onDestroy, onMount } from 'svelte';

  let sectionNodes: NodeListOf<HTMLElement>;
  let sectionObserver: IntersectionObserver;

  
  onMount(() => {
    sectionObserver = new IntersectionObserver(
      (entries: IntersectionObserverEntry[]) => {
        const allVisibleSections: IntersectionObserverEntry[] = entries.filter((entry: IntersectionObserverEntry) => entry.isIntersecting);
        if (allVisibleSections.length === 0) {
          return;
        }
        allVisibleSections.forEach((container: IntersectionObserverEntry) => {
          container.target.classList.add('project-div-anim');
        });
      },
      { threshold: 0.01 },
    );
    sectionNodes = document.querySelectorAll('.project-div');
    sectionNodes.forEach((section: HTMLElement) => sectionObserver.observe(section));
  });

  onDestroy(() => {
    sectionNodes.forEach((section: HTMLElement) => sectionObserver.unobserve(section));
  });
  */
</script>

<div class="project-div">
  <div class="project-section">
    <div class="project-details">
      <div class="project-info">
        <span class="project-title">Digital Kampung</span>
        <div class="project-divider" />
        <span class="project-text">
          An online platform that enables users to search for and rate/review hawker stalls across Singapore.
          <br />
          <strong>Tech Stack: React, Express, PostgreSQL, NodeJS</strong>
        </span>
      </div>
      <img class="project-img" alt="" src="/img/projects/digitalkampung-img.png" />
    </div>
    <div class="project-links">
      <a class="project-button" href={$url('/projects')}>About Project</a>
      <a class="project-button" href="https://digital-kampung.netlify.app/">Live Website</a>
      <a class="project-button" href="https://github.com/DigitalKampong">Source Code</a>
    </div>
  </div>
  <div class="project-section">
    <div class="project-details">
      <div class="project-info">
        <span class="project-title">CULLinary Series</span>
        <div class="project-divider" />
        <span class="project-text">
          The CULLinary series is a game series that combines aspects of a Dungeon Crawler and a Food Delivery/Restaurant Simulator.
          <br />
          <strong>Tech Stack: Unity</strong>
        </span>
      </div>
      <img class="project-img" alt="" src="/img/projects/cullinary2-img.png" />
    </div>
    <div class="project-links">
      <a class="project-button" href={$url('/projects')}>About Project</a>
      <a class="project-button" href="https://github.com/AngryEggplantStudios">Source Code</a>
      <a class="project-button" href={$url('/projects/cull1')}>Play CULLinary</a>
      <a class="project-button" href={$url('/projects/cull2')}>Play CULLinary2</a>
    </div>
  </div>
  <div class="project-section">
    <div class="project-details">
      <div class="project-info">
        <span class="project-title">Project Kampong</span>
        <div class="project-divider" />
        <span class="project-text">
          Project Kampong is an online collaborative platform that serves as a digital aggregator to effectively map assets across communities and
          establish a data and documentation center for the Social Sector to provide clarity in needs, resources and gaps.
          <br />
          <strong>Tech Stack: Angular, NestJS, GraphQL, MongoDB</strong>
        </span>
      </div>
      <img class="project-img" alt="" src="/img/projects/kampong-img.png" />
    </div>
    <div class="project-links">
      <a class="project-button" href={$url('/projects')}>About Project</a>
      <a class="project-button" href="https://github.com/Project-Kampong">Source Code</a>
    </div>
  </div>
  <div class="project-section">
    <div class="project-details">
      <div class="project-info">
        <span class="project-title">SafeSpace</span>
        <div class="project-divider" />
        <span class="project-text">
          SafeSpace is a VR Mental Health Simulator and Meditation Guide that aims to enhance awareness and understanding of anxiety disorders through
          two modes of gameplay
          <br />
          <strong>Tech Stack: Unity, SRanipal, TobiiXR SDKs </strong>
        </span>
      </div>
      <img class="project-img" alt="" src="/img/projects/safespace-img.png" />
    </div>
    <div class="project-links">
      <a class="project-button" href={$url('/projects')}>About Project</a>
      <a class="project-button" href="https://github.com/Kalsyc/SafeSpace">Source Code</a>
    </div>
  </div>
</div>

<style>
  .project-div {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 2em 20%;
  }

  :global(.project-div-anim) {
    -webkit-animation: fadein 2s;
    -moz-animation: fadein 2s;
    -ms-animation: fadein 2s;
    -o-animation: fadein 2s;
    animation: fadein 2s;
  }

  .project-section {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    width: 70vw;
    max-width: 70vw;
    background-color: #efe2ba;
    border-radius: 1em;
    padding: 1.5em;
    border: #e87121 3px solid;
    margin: 1em 0;
  }

  .project-details {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: space-between;
    width: inherit;
    max-width: inherit;
  }

  .project-divider {
    border: #e87121 1px solid;
    width: 100%;
    height: 0;
    margin: 5px 0;
  }

  .project-title {
    font-weight: 700;
    font-size: 1.5rem;
    color: #e87121;
  }

  .project-info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    text-align: left;
  }

  .project-img {
    object-fit: contain;
    height: 125px;
    width: 200px;
    padding: 1em;
  }

  .project-text {
    color: #2c3e50;
    margin: 0.5em 0;
  }

  .project-links {
    display: flex;
    flex-direction: row;
  }

  .project-button {
    color: #2c3e50;
    font-weight: 700;
    font-size: 1.1rem;
    color: #e87121;
    padding: 0 1em 0 0;
  }

  .project-button:hover {
    cursor: pointer;
  }

  @media screen and (max-width: 600px) {
    .project-details {
      flex-direction: column-reverse;
      align-items: center;
    }

    .project-links {
      flex-direction: column;
    }
    .project-button {
      padding: 0.5em 0;
    }
    .project-section {
      align-items: center;
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

  @-moz-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @-webkit-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @-ms-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @-o-keyframes fadein {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
</style>

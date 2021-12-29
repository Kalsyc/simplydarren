<script lang="ts">
  import HeaderComponent from '../components/HeaderComponent.svelte';
  import FooterComponent from '../components/FooterComponent.svelte';
  import { metatags } from '@roxi/routify';
  import { onMount } from 'svelte';

  metatags.title = 'About';

  let currentNav: string = 'bio-circle';

  onMount(() => {
    let navItemNodes: NodeListOf<Element> = document.querySelectorAll('.about-nav-link');
    let navItemArr: Element[] = Array.from(navItemNodes);
    navItemArr.forEach((ele: Element) => {
      ele.addEventListener('click', (e: Event) => {
        const elementId: string = (e.target as Element).id;
        if (currentNav != elementId) {
          document.getElementById(currentNav).classList.remove('link-circle-selected');
        }
        currentNav = elementId;
        document.getElementById(currentNav).classList.add('link-circle-selected');
      });
    });
  });
</script>

<main>
  <HeaderComponent />
  <div class="about-main-div">
    <nav class="about-nav">
      <div class="about-nav-item">
        <a href="#bio" class="about-nav-link"><div class="link-circle link-circle-selected" id="bio-circle" /></a>
        <span class="about-nav-label">Bio</span>
      </div>
      <div class="about-nav-item">
        <a href="#education" class="about-nav-link"><div class="link-circle" id="education-circle" /></a>
        <span class="about-nav-label">Education</span>
      </div>
      <div class="about-nav-item">
        <a href="#work" class="about-nav-link"><div class="link-circle" id="work-circle" /></a>
        <span class="about-nav-label">Work Experience</span>
      </div>
      <div class="about-nav-item">
        <a href="#teaching" class="about-nav-link"><div class="link-circle" id="teaching-circle" /></a>
        <span class="about-nav-label">Teaching Experience</span>
      </div>
      <div class="about-nav-item">
        <a href="#skills" class="about-nav-link"><div class="link-circle" id="skills-circle" /></a>
        <span class="about-nav-label">Skills</span>
      </div>
      <div class="about-nav-item">
        <a href="#projects" class="about-nav-link"><div class="link-circle" id="projects-circle" /></a>
        <span class="about-nav-label">Projects</span>
      </div>
      <div class="about-nav-item">
        <a href="#contact" class="about-nav-link"><div class="link-circle" id="contact-circle" /></a>
        <span class="about-nav-label">Contact Me</span>
      </div>
    </nav>
    <div class="about-main-body">
      <div class="about-section about-bio-div" id="bio" data-label="bio">Bio</div>
      <div class="about-section about-education-div" id="education" data-label="education">Education</div>
      <div class="about-section about-work-div" id="work" data-label="work">Work Experience</div>
      <div class="about-section about-teaching-div" id="teaching" data-label="teaching">Teaching Experience</div>
      <div class="about-section about-skills-div" id="skills" data-label="skills">Skills</div>
      <div class="about-section about-projects-div" id="projects" data-label="projects">Projects</div>
      <div class="about-section about-contact-div" id="contact" data-label="contact">Contact Me</div>
    </div>
  </div>
  <FooterComponent />
</main>

<style>
  .about-main-div {
    display: flex;
    flex-direction: column;
    text-align: center;
    min-height: 100vh;
  }

  .about-nav {
    padding: 1.5em;
    position: fixed;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
  }

  .about-nav-label {
    color: #e87121;
    font-weight: 700;
    font-size: 0.9rem;
    opacity: 0;
    transition: opacity 0.1s;
  }

  .about-nav-link {
    margin: 0.5em 0.75em 0.5em 0;
    scroll-behavior: smooth;
  }

  .link-circle {
    background-color: #e87121;
    opacity: 0.5;
    border-radius: 50%;
    height: 15px;
    width: 15px;
    transition: transform 0.2s;
  }

  .link-circle-selected {
    opacity: 1;
    background-color: #e87121;
    transform: scale(1.35);
  }

  .about-nav-link:hover ~ .about-nav-label {
    opacity: 1;
  }

  .about-nav-item {
    display: flex;
    align-items: center;
    margin-bottom: 0.5em;
  }

  .about-section {
    min-height: 100vh;
  }

  .about-bio-div {
    background-color: aliceblue;
  }

  .about-education-div {
    background-color: antiquewhite;
  }

  .about-work-div {
    background-color: aqua;
  }

  .about-teaching-div {
    background-color: aquamarine;
  }

  .about-skills-div {
    background-color: azure;
  }

  .about-projects-div {
    background-color: beige;
  }

  .about-contact-div {
    background-color: bisque;
  }
</style>

<div class="skills-div">
  <span class="skilltype-title">Framework & Tools</span>
  <div class="skills-grid">
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/react-icon.png" />
      <span class="skill-text">React</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/angular-icon.svg" />
      <span class="skill-text">Angular</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/svelte-icon.png" />
      <span class="skill-text">Svelte</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/unity-icon.png" />
      <span class="skill-text">Unity</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/nodejs-icon.png" />
      <span class="skill-text">NodeJS</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/electron-icon.png" />
      <span class="skill-text">Electron</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/adobexd-icon.png" />
      <span class="skill-text">Adobe XD</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/figma-icon.png" />
      <span class="skill-text">Figma</span>
    </div>
  </div>
  <span class="skilltype-title">Languages</span>
  <div class="skills-grid">
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/typescript-icon.png" />
      <span class="skill-text">TypeScript</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/javascript-icon.png" />
      <span class="skill-text">JavaScript</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/python-icon.png" />
      <span class="skill-text">Python</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/csharp-icon.png" />
      <span class="skill-text">C#</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/html-icon.png" />
      <span class="skill-text">HTML5</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/css-icon.jpeg" />
      <span class="skill-text">CSS3</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/postgresql-icon.png" />
      <span class="skill-text">PostgreSQL</span>
    </div>
    <div class="skill-cell">
      <img class="skill-img" alt="" src="/img/java-icon.png" />
      <span class="skill-text">Java</span>
    </div>
  </div>
</div>

<style>
  .skills-div {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 2em 20%;
    text-align: left;
  }

  .skilltype-title {
    color: #e87121;
    font-weight: 700;
    font-size: 1.5rem;
    margin-top: 0.5em;
  }

  .skills-grid {
    padding: 1em 0;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    border-radius: 10px;
  }

  .skill-cell {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0.5em;
  }

  .skill-text {
    padding: 0.5em 0;
    opacity: 1;
  }

  .skill-img {
    height: 75px;
    width: 75px;
    aspect-ratio: 1;
    object-fit: contain;
  }

  @media only screen and (min-width: 600px) {
    .skills-grid {
      grid-template-columns: repeat(4, 1fr);
    }
  }

  @media only screen and (min-width: 800px) {
    .skills-grid {
      grid-template-columns: repeat(6, 1fr);
    }
    .skill-text {
      opacity: 0;
    }

    .skill-img:hover ~ .skill-text {
      transition: ease-in 0.3s;
      opacity: 1;
    }
  }

  @media only screen and (min-width: 1200px) {
    .skills-grid {
      grid-template-columns: repeat(8, 1fr);
    }
  }
</style>

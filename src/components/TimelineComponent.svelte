<div class="timeline-div">
  <div class="timeline-container left">
    <div class="timeline-content">
      <span class="timeline-title">Began College</span>
      <div class="timeline-divider" />
      <span class="timeline-date">Aug 2018</span>
      <span class="timeline-text">Matriculated as a Computer Science Major in 2018 at the National University of Singapore (NUS).</span>
    </div>
  </div>
  <div class="timeline-container right">
    <div class="timeline-content">
      <span class="timeline-title">WaveScan Technologies Pte. Ltd</span>
      <span class="timeline-designation">UI/UX Developer Intern</span>
      <div class="timeline-divider" />
      <span class="timeline-date">May 2020 - Dec 2020</span>
      <span class="timeline-text">
        <ul>
          <li>Joined Singapore-based startup WaveScan as an UI/UX Developer in May 2020</li>
          <li>
            Maintained a brown-field Electron application that performs volumetric rendering and image analysis of 3D-scanned data using VTKjs with
            React
          </li>
          <li>
            Developed a green-field Electron web application that is integrated into a robotic scanner with a RPi4 from ideation phase to a working
            beta product
          </li>
          <li>Integrated libraries/frameworks such as Redux, VTKjs, Plotly and Konvajs to optimise performance and improve maintainability</li>
          <li>Spearheaded the redesign and prototyping in Adobe XD for both applications</li>
        </ul>
      </span>
    </div>
  </div>
  <div class="timeline-container left">
    <div class="timeline-content">
      <span class="timeline-title">STUCK Design</span>
      <span class="timeline-designation">Full Stack Developer Intern</span>
      <div class="timeline-divider" />
      <span class="timeline-date">May 2021 - Sep 2021 </span>
      <span class="timeline-text">
        <ul>
          <li>Joined Singapore-based Industrial Design company STUCK Design as a Full Stack Developer Intern in May 2021</li>
          <li>
            Developed a Unity application for the iPad that brings creative artworks to life for children to discover and explore via touch gestures
          </li>
          <li>Maintained and fixed bugs arising from existing applications</li>
          <li>Implemented a web application in Svelte for checking dine-in rules for vaccinated people</li>
        </ul>
      </span>
    </div>
  </div>
  <div class="timeline-container right">
    <div class="timeline-content">
      <span class="timeline-title">Graduation (Pending)</span>
      <div class="timeline-divider" />
      <span class="timeline-date">May 2022</span>
      <span class="timeline-text">Due to graduate from NUS with a Bachelor of Computing (Distinction) in Computer Science in May 2022</span>
    </div>
  </div>
</div>

<style>
  * {
    box-sizing: border-box;
  }

  .timeline-div {
    position: relative;
    max-width: 60vw;
    margin: 2em auto;
  }

  .timeline-divider {
    border: 1px solid #e87121;
    height: 0;
    opacity: 50%;
    width: 100%;
  }

  .timeline-div::after {
    content: '';
    position: absolute;
    width: 6px;
    background-color: #e87121;
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -3px;
  }

  .timeline-container {
    padding: 10px 40px;
    position: relative;
    background-color: inherit;
    width: 50%;
  }

  .timeline-container::after {
    content: '';
    position: absolute;
    width: 25px;
    height: 25px;
    right: -17px;
    background-color: #e87121;
    border: 4px solid #e87121;
    top: 15px;
    border-radius: 50%;
    z-index: 1;
  }

  .left {
    left: 0;
  }

  .right {
    left: 50%;
  }

  .left::before {
    content: ' ';
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    right: 30px;
    border: medium solid #efe2ba;
    border-width: 10px 0 10px 10px;
    border-color: transparent transparent transparent #efe2ba;
  }

  .right::before {
    content: ' ';
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    left: 30px;
    border: medium solid #efe2ba;
    border-width: 10px 10px 10px 0;
    border-color: transparent #efe2ba transparent transparent;
  }

  .right::after {
    left: -16px;
  }

  .timeline-content {
    padding: 20px;
    background-color: #efe2ba;
    position: relative;
    border-radius: 6px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    text-align: left;
  }

  .timeline-title {
    color: #e87121;
    font-weight: 700;
    font-size: 1.25rem;
  }

  .timeline-date,
  .timeline-designation {
    color: #e87121;
    font-weight: 500;
    font-size: 1.1rem;
  }

  .timeline-text {
    font-size: 0.85rem;
  }

  .timeline-text > ul {
    margin-block: 0.2em;
    padding-inline-start: 1.5em;
  }

  @media screen and (max-width: 600px) {
    .timeline-div {
      max-width: 85vw;
    }
  }

  @media screen and (max-width: 800px) {
    .timeline-div::after {
      left: 31px;
    }

    .timeline-container {
      width: 100%;
      padding-left: 70px;
      padding-right: 25px;
    }

    .timeline-container::before {
      left: 60px;
      border: medium solid white;
      border-width: 10px 10px 10px 0;
      border-color: transparent #efe2ba transparent transparent;
    }

    .timeline-content {
      padding: 10px;
    }

    .left::after,
    .right::after {
      left: 15px;
    }

    .right {
      left: 0%;
    }
  }
</style>

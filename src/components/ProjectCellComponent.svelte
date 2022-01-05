<script lang="ts">
  import { url } from '@roxi/routify';

  export let projectParam: string;
  export let projectImgPath: string;
  export let projectTitle: string;
  export let projectDesc: string;
  export let projectType: string;
  export let projectTag: string;
</script>

<div class="completed-cell">
  <a href={$url('/projects/:project', { project: projectParam })}>
    <img class="completed-img" alt="" src={projectImgPath} />
    <div class="completed-overlay">
      <div class="completed-tag {projectType}">{projectTag}</div>
      <div class="completed-text">
        <div class="completed-title">
          {projectTitle}
        </div>
        <div class="completed-desc">
          {projectDesc}
        </div>
      </div>
    </div>
  </a>
</div>

<style>
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

  .completed-img {
    display: block;
    height: 225px;
    width: 400px;
    aspect-ratio: 1;
    object-fit: cover;
    border-radius: 1em;
  }

  .completed-tag {
    position: absolute;
    top: 3%;
    left: 3%;
    color: white;
    font-weight: 700;
    border-radius: 10px;
    padding: 0 0.5em;
    width: fit-content;
  }

  .completed-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
  }

  .completed-title,
  .completed-desc {
    color: white;
    font-weight: 700;
    font-size: 1.25rem;
    padding: 0 0.75em;
  }

  .webdev {
    background-color: #26a400;
  }

  .uiux {
    background-color: #e87121;
  }

  .gamedev {
    background-color: #0118e2;
  }

  .appdev {
    background-color: #e70013;
  }

  .vr {
    background-color: #7000ad;
  }

  @media screen and (max-width: 900px) {
    .completed-overlay {
      top: 50%;
      height: 50%;
      opacity: 1;
      display: flex;
      flex-direction: column;
    }

    .completed-text {
      align-items: flex-start;
      justify-content: center;
    }

    .completed-title,
    .completed-desc {
      text-overflow: ellipsis;
      overflow: hidden;
      white-space: nowrap;
      font-size: 1rem;
    }

    .completed-tag {
      top: 0;
      left: 0;
      border-radius: 10px 0 0 0;
      position: relative;
      width: fit-content;
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
      max-width: fit-content;
    }

    .completed-title,
    .completed-desc {
      text-align: left;
    }
  }

  @media screen and (max-width: 400px) {
    .completed-tag {
      font-size: 0.75rem;
    }

    .completed-title {
      font-size: 0.8rem;
      text-overflow: ellipsis;
      overflow: hidden;
      white-space: nowrap;
    }

    .completed-desc {
      display: none;
    }
  }
</style>

<template>
  <section class="portfolio">
    <base-heading is-light-text>Portfolio</base-heading>
    <div class="projects">
      <div
        v-for="(project, index) in myProjects"
        :key="index"
        class="project-tile">
        <a
          :href="project.href"
          target="_blank"
          rel="noopener"
          class="project">
          <img
            :src="project.image"
            :alt="project.title"
            class="project-image">
          <div class="project-overlay">
            <h3 class="project-title">{{ project.title }}</h3>
            <p class="project-description">{{ project.description }}</p>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import BaseHeading from '@/components/BaseHeading'
import { projects } from '@/utils'

export default {
  name: 'BasePortfolioPreview',
  components: {
    BaseHeading,
  },
  computed: {
    myProjects() {
      return projects
    },
  },
}
</script>

<style lang="postcss" scoped>
.portfolio {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: var(--bgColorDark);
  color: var(--lightText);
  padding: 100px 15px;
}

.projects {
  display: flex;
  flex-direction: column;
}

@media (min-width: 768px) {
  .projects {
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    max-width: 675px;
    padding: 0 15px;
  }
}

@media (min-width: 992px) {
  .projects {
    max-width: 900px;
  }
}

@media (min-width: 1200px) {
  .projects {
    max-width: 1200px;
  }
}

.project-tile {
  padding: 20px 0;
}

@media (min-width: 768px) {
  .project-tile {
    padding: 20px;
  }
}

.project {
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--lightText);
  text-decoration: none;
  width: 300px;
  height: 200px;
  position: relative;
  overflow: hidden;
  border: 3px solid #2980b9;
}

@media (min-width: 992px) {
  .project:hover {
    cursor: pointer;
    border: 3px solid #3498db;
  }
}

.project-image {
  width: 100%;
  height: 100%;
  transition: all 0.2s linear;
}

.project-image:hover {
  transform: scale(1.1);
}

.project-overlay {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: var(--transparentDarkBlue);
  color: var(--lightText);
  padding: 15px;
}

@media (min-width: 992px) {
  .project-overlay {
    opacity: 0;
    transition: all 0.15s ease;
  }

  .project-overlay:hover {
    opacity: 1;
    transition: opacity 0.2s linear;
  }

  .project-overlay:hover > .project-title {
    opacity: 1;
    transform: translateY(0);
    transition: all 0.3s ease-in-out;
  }

  .project-overlay:hover > .project-description {
    opacity: 1;
    transform: translateY(0);
    transition: all 0.3s 0.1s ease-in-out;
  }
}

.project-title {
  font-family: OpenSans-Bold;
  font-size: 24px;
  text-transform: uppercase;
}

@media (min-width: 992px) {
  .project-title {
    opacity: 0;
    transform: translateY(-100px);
    transition: all 0.3s ease-in-out;
  }
}

.project-description {
  font-size: 12px;
  font-family: Lora-Regular;
  line-height: 20px;
}

@media (min-width: 992px) {
  .project-description {
    font-size: 14px;
    opacity: 0;
    transform: translateY(100px);
    transition: all 0.3s ease-in-out;
  }
}
</style>

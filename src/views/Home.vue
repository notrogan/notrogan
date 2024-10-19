<template>
  <ion-page>
    <ion-content>

      <div style="background-color: white;">
        <div class="about">
          <div class="hoist">
            <About/>
          </div>
          <div class="buffer"></div>
        </div>
      </div>

      <div style="background-color: #101014;">
        <div class="projects">
          <div class="semi-circle"></div>
          <div class="projects-header-wrapper">
            <div class="projects-header">
              Projects
            </div>
            <div class="projects-subheader">
              Stuff that works, sometimes.
            </div>
          </div>
          <div class="project">
            <div class="hoist" style="margin-top: 4rem;">
              <Project/>
            </div>
          </div>
          <div class="buffer"></div>
        </div>
      </div>

    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';

import About from './components/About.vue';
import Project from './components/Project.vue';

</script>

<style scoped>

.about {
  .hoist {
    top: 0rem;
    height: 100vh;
    position: sticky;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  .buffer {
    height: 100vh;
  }
}

.project {
  background: linear-gradient(180deg, rgba(0,0,0,0) 20%, #101014 20%, #101014 100%);

  .hoist {
    display: flex;
    align-items: center;
    justify-content: center;
  }
}

.projects {
  width: 100%;

  transform: translateY(-50rem);
  position: absolute;
  
  .projects-header-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;

    .projects-header {
      position: absolute;
      margin-bottom: 15rem;

      color: white;
      font-size: 7rem;
      font-family: "rivian-bold";
    }

    .projects-subheader {
      position: absolute;
      margin-bottom: 0rem;

      color: white;
      font-size: 2.5rem;
      font-family: "rivian";
    }
  }

  .semi-circle {
    width: 105%;
    height: 120rem;

    left: 50%;
    position: absolute;
    background-color: #101014;
    
    clip-path: ellipse(60% 40% at 50% 100%);
    transform: translateY(-73%) translateX(-50%);
  }
}

@font-face {
  font-family: 'rivian-bold';
  src: url('../font/Halbfett.otf');
  font-weight: normal;
  font-style: normal;
}

</style>

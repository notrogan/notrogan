<template>
  <ion-page>
    <ion-content>
      <div style="background-color: #fefeff;">
        <div class="about">
          <About/>
        </div>
      </div>
      <div style="background-color: #fefeff;">
        <div class="semi">
          
        </div>

        <div class="hoist">
          <img class="lethal-transition" src="../img/lethal/header.png">
          <img class="lethal-logo" src="../img/lethal/logo.png">
        </div>
        
        <div style="height: 125vh;"></div>
      </div>
      <div>
        <div style="height: 5vh; background-color: #000000;"></div>
        <Project/>
      </div>

    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';

import About from './components/About.vue';
import Meet from './components/Meet.vue';
import Project from './components/Project.vue';

</script>

<style scoped lang="css">

@keyframes slide-lethal {
  20% {
    transform: translateY(-100%);
  }
  95% {
    transform: translateY(0%);
  }
}

@keyframes fade-lethal {
  15% {
    filter: brightness(1);
  }
  100% {
    filter: brightness(50%);
  }
}

.about {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50vh;
}

.hoist {
  top: 0vh;
  height: 100vh;
  position: sticky;

  display: flex;
  align-items: center;
  justify-content: center;

  .lethal-logo {
    animation: slide-lethal ease-out forwards;
    animation-timeline: view();
    animation-range: cover 70vh cover 175vh;

    position: absolute;
    filter: drop-shadow(0 0 .75rem rgb(0, 0, 0));
  }

  .lethal-header {
    animation: slide-header-lethal ease-out forwards;
    animation-timeline: view();
    animation-range: cover 70vh cover 175vh;

    position: absolute;
    filter: drop-shadow(0 0 .75rem rgb(0, 0, 0));

    position: absolute;
    transform: translateY(300%);
    font-size: 3.5rem;
    font-family: 'company-regular';
  }

  .lethal-transition {
    animation: fade-lethal ease-in-out forwards;
    animation-timeline: view();
    animation-range: cover 135vh cover 215vh;

    width: 100vw;
    height: 101vh;
    object-fit: cover;
  }
}

.header {
  height: 70vh;
  background-color: #000000;

  .main {
    color: white;
    margin-left: 4vw;
    font-size: 11rem;
    font-family: "rivian";
    transform: translateY(3vh);
  }

  .sub {
    color: white;
    margin-left: 4vw;
    font-size: 11rem;
    font-family: "rivian";
    transform: translateY(-3vh);
  }

  .blurb {
    width: 23%;
    float: right;
    color: white;
    margin-top: 10vh;
    margin-right: 3vw;
    font-size: 1.4rem;
    font-family: "rivian";
    transform: translateY(-6vh);
  }
}

.semi {
  z-index: 1;
  height: 80vh;
  width: 140vw;
  position: absolute;
  background-color: #fefeff;
  transform: translateX(-20vw) translateY(-5vh);
  clip-path: ellipse(50% 100% at 50% 0%);
}

@font-face {
  font-family: 'rivian-bold';
  src: url('../font/Halbfett.otf');
  font-weight: normal;
  font-style: normal;
}

</style>

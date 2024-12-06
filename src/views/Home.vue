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
          <img class="transition" src="../img/download.png">
        </div>
        
        <div style="height: 100vh;"></div>
      </div>
      <div class="project">
        <div class="header">
          <div class="main">
            Projects that arent
          </div>
          <div class="sub">
            terrible
          </div>
          <div class="blurb">
            We listened and learned to craft a vehicle fit for adventures of all kinds. R2 has everything you need to get out there and say yes to new things.
          </div>
        </div>
      </div>
      <div style="background-color: #141415;">
        <div style="height: 5vh;"></div>
      </div>
      <div style="background-color: #141415;">
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

<style scoped>

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

  .transition {
    width: 100vw;
    height: 101vh;
    object-fit: cover;
  }
}

.header {
  height: 70vh;
  background-color: #141415;

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

.pill {
  .hoist {
    top: 0rem;
    height: 100vh;
    position: sticky;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  .buffer {
    height: 60vh;
  }

  .transition {
    margin: 0 auto;
    display: block;
    
    object-fit: cover;

    animation: pill linear forwards;
    animation-timeline: view();
    animation-range: cover 83vh cover 150vh;

    opacity: 1;
    width: 80vw;
    height: 60vh;
    position: relative;
    border-radius: 350px;
  }
}

@keyframes pill {
  0% {
    opacity: 1;
    width: 80vw;
    height: 60vh;
    position: relative;
    border-radius: 350px;
  }
  30% {
    width: 90vw;
    height: 80vh;
    border-radius: 400px;
  }
  60% {
    width: 95vw;
    height: 90vh;
    border-radius: 450px;
  }
  100% {
    width: 100%;
    display: flex;
    height: 100vh;
    border-radius: 0;
  }
}

@font-face {
  font-family: 'rivian-bold';
  src: url('../font/Halbfett.otf');
  font-weight: normal;
  font-style: normal;
}

</style>

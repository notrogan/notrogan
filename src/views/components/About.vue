<script setup lang="ts">
import { IonGrid, IonRow, IonCol } from '@ionic/vue';

</script>

<template>
  <div class="wrapper">
    <div class="about">
      <IonGrid>
        <IonRow>
          <IonCol size="auto">
            <div class="image-wrapper">
              <img class="image" src="../../img/about/profile.gif">
            </div>
          </IonCol>
          <IonCol>
            <div class="text-wrapper">
              <div class="header">
                Hello!
              </div>
              <div class="main">
                Pretend there are words here words words words words words words words words words
              </div>
            </div>
          </IonCol>
        </IonRow>
      </IonGrid>
    </div>
  </div>
</template>

<style scoped>

.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;

  z-index: 999;
  overflow: visible;
  transform: translateY(25vh);

  .about {
    width: 50%;
    min-width: 50rem;

    .image-wrapper { 
      margin: 2%;
      max-width: 15rem;
      max-height: 15rem;

      .image {
        border-radius: 10%;
        -webkit-user-drag: none;
      }
    }

    .text-wrapper {
      margin-left: 2%;

      .header {
        color: black;
        font-size: 2.5rem;
        font-family: "rivian-bold", "aileron-bold";
      }

      .main {
        color: black;
        font-size: 1.5rem;
        font-family: "rivian";
      }
    }
  }
}

@font-face {
  font-family: 'rivian';
  src: url('../../font/Kraftig.otf');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'rivian-bold';
  src: url('../../font/Halbfett.otf');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'aileron-bold';
  src: url('../../font/Aileron.otf');
  font-weight: normal;
  font-style: normal;
}

</style>

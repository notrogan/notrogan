<script setup lang="ts">
import { IonGrid, IonRow, IonCol } from '@ionic/vue';
import { defineComponent, onMounted } from 'vue';

let latestCruiserCourier = "";
let latestFirstPersonDeath = ""

const fetchVersion = async (name: string) => {
  const response = await fetch(`https://thunderstore.io/api/experimental/package/rogan/${name}/`);
  const baseJson = await response.json();

  if (name == "CruiserCourier") {
    latestCruiserCourier = baseJson['latest']['version_number'];
  }
  else if (name == "FirstPersonDeath") {
    latestFirstPersonDeath = baseJson['latest']['version_number'];
  }
}

onMounted(() => {
  fetchVersion("CruiserCourier");
  fetchVersion("FirstPersonDeath");
})

</script>

<template>
  <div class="wrapper">
    <IonGrid>
      <IonRow class="item">
        <IonCol size="auto">
          <div class="image-wrapper">
            <img class="image" src="../../img/lethal/spoiler.gif">
          </div>
        </IonCol>
        <IonCol>
          <div class="text-wrapper">
            <div class="header">
              First Person Death
            </div>
            <div class="main">
              i dont feel like writing the descriptions for these... might add later :D
            </div>
          </div>
          <a class="button-wrapper" href="https://github.com/notrogan/FirstPersonDeath" target="_blank" rel="noreferrer noopener">
            <div class="button">
              <div class="button-text">
                View on GitHub
              </div>
            </div>
          </a>
        </IonCol>
      </IonRow>
    </IonGrid>
  </div>
</template>

<style scoped>


.button-wrapper {
  margin-top: 1rem;
  margin-left: 1rem;
  display: flex;
  text-align: center;
  text-decoration: none;

  .button {
    width: 40%;
    height: 4vh;
    border-radius: 6vh;
    transition: all .5s ease;
    border: 2px solid white;

    .button-text {
      color: white;
      font-size: 1.5rem;
      user-select: none;
      margin-top: .25rem;
      transition: all .5s ease;
      font-family: "rivian", "aileron-bold";
    }
  }
}

.button-wrapper:hover {
	.button {
		background-color: white;
		.button-text {
			filter: invert(1);
		}
	}
}

.wrapper {
  background-color: #000000;

  .item {
    width: 50%;
    margin: auto;

    .image-wrapper { 
      margin: 2%;
      max-width: 15rem;
      max-height: 15rem;

      .image {
        width: 15rem;
        border-radius: 10%;
        -webkit-user-drag: none;
      }
    }

    .text-wrapper {
      margin-left: 2%;

      .header {
        color: #fefeff;
        font-size: 2.5rem;
        font-family: "rivian-bold", "aileron-bold";
      }

      .main {
        color: #fefeff;
        font-size: 1.5rem;
        font-family: "rivian", "aileron-bold";
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

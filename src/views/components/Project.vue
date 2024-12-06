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
    <div class="project">
      <IonGrid style="width: 92%;">
        <IonRow>
          <IonCol size="7">
            <img class="image" src="../../img/gallery_1.jpg">
          </IonCol>
          <IonCol>
            <div style="display: flex;">
              <div class="header" style="margin-left: 2rem;">
                Cruiser Courier
              </div>
              <div class="version">
                {{ latestCruiserCourier }}
              </div>
            </div>
            <div class="sub" style="margin-left: 2rem;">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
            </div>
						<a class="button-wrapper" href="https://github.com/notrogan/CruiserCourier" target="_blank" rel="noreferrer noopener">
							<div class="button">
								<div class="button-text">
									View on GitHub
								</div>
							</div>
						</a>
          </IonCol>
        </IonRow>
        
        <div style="height: 5vh;"></div>

        <IonRow>
          <IonCol>
            <div style="display: flex;">
              <div class="header" style="margin-left: 2rem;">
                First Person Death
              </div>
              <div class="version">
                {{ latestFirstPersonDeath }}
              </div>
            </div>
            <div class="sub" style="text-align: right; margin-right: 2rem">
              
            </div>
						<a class="button-wrapper" style="float: right;" href="https://github.com/notrogan/FirstPersonDeath" target="_blank" rel="noreferrer noopener">
							<div class="button">
								<div class="button-text">
									View on GitHub
								</div>
							</div>
						</a>
          </IonCol>
          <IonCol size="7">
            <img class="image" src="../../img/gallery_1.jpg">
          </IonCol>
        </IonRow>
      </IonGrid>
    </div>
  </div>
</template>

<style scoped>

.wrapper {
  .project {
    .image {
      width: 100%;
      float: right;
      height: 50vh;
      margin-top: 1rem;
      margin-left: 1rem;
      object-fit: cover;
      margin-bottom: 1rem;
      border-radius: 1.5rem;
    }

    .header {
      color: white;
      margin-top: 1rem;
      font-size: 3.5rem;
      font-family: "rivian-bold";
      transform: translateY(-12.5%);
    }

    .version {
      color: #ffffff;
      margin-top: 1rem;
      margin-left: 1rem;
      font-size: 3.5rem;
      font-family: "rivian-bold";
      transform: translateY(-12.5%);
    }

    .sub {
      color: white;
      font-size: 1.5rem;
      font-family: "rivian";
    }

    .button-wrapper {
			width: 50%;
			margin-top: 1.25rem;
			margin-left: 2rem;
      margin-right: 2rem;

			display: flex;
			text-align: center;
			align-items: center;
			text-decoration: none;
			justify-content: center;

			.button {
				width: 100%;
				height: 5vh;
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

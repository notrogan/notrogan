<script setup lang="ts">
import { IonGrid, IonRow, IonCol } from '@ionic/vue';

</script>

<template>
  <div class="wrapper">
    <div class="project">
			<IonGrid>
				<IonRow>
					<IonCol>
						<div class="header-wrapper">
							Lethal Company
						</div>
					</IonCol>
				</IonRow>
				<IonRow>
					<IonCol size="auto">
						<div class="image-wrapper">
							<img class="image" src="../../img/about/profile.gif">
						</div>
					</IonCol>
					<IonCol>
						<div class="text-wrapper">
							<div class="header">
								First Person Death
							</div>
							<div class="main">
								Simple mod that re-enables the first person camera after death instead of using the default spectator camera; Lightweight, configurable, and client-sided!
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
				<IonRow>
					<IonCol size="auto">
						<div class="image-wrapper">
							<img class="image" src="../../img/about/profile.gif">
						</div>
					</IonCol>
					<IonCol>
						<div class="text-wrapper">
							<div class="header">
								No Fox
							</div>
							<div class="main">
								Hate the kidnapper fox? Me too. This mod disables both the fox and vain shrouds so that you never have to see that abomination again; Simple and server-sided!
							</div>
						</div>
						<a class="button-wrapper" href="https://github.com/notrogan/NoFox" target="_blank" rel="noreferrer noopener">
							<div class="button">
								<div class="button-text">
									View on GitHub
								</div>
							</div>
						</a>
					</IonCol>
				</IonRow>
			</IonGrid>
			<div class="buffer"></div>
			<IonGrid>
				<IonRow>
					<IonCol>
						<div class="header-wrapper">
							Counter Strike
						</div>
					</IonCol>
				</IonRow>
				<IonRow>
					<IonCol size="auto">
						<div class="image-wrapper">
							<img class="image" src="../../img/about/profile.gif">
						</div>
					</IonCol>
					<IonCol>
						<div class="text-wrapper">
							<div class="header">
								First Person Death
							</div>
							<div class="main">
								Simple mod that re-enables the first person camera after death instead of using the default spectator camera; Lightweight, configurable, and client-sided!
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
  </div>
</template>

<style scoped>

.header-wrapper {
	color: white;
	font-size: 3.5rem;
	margin-left: 0.75rem;
	font-family: "rivian-bold", "aileron-bold";
}

.buffer {
	height: 2rem;
}

.wrapper {
	display: flex;
	align-items: center;
	justify-content: center;

	.project {
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
			margin-top: 0.4rem;

			.header {
				color: white;
				font-size: 2.5rem;
				font-family: "rivian-bold", "aileron-bold";
			}

			.main {
				color: white;
				font-size: 1.5rem;
				margin-top: 0.25rem;
				font-family: "rivian", "aileron";
			}
		}

		.button-wrapper {
			width: 50%;
			margin-top: 1rem;
			margin-left: 0.5rem;

			display: flex;
			text-align: center;
			align-items: center;
			text-decoration: none;
			justify-content: center;

			.button {
				width: 100%;
				height: 2.9rem;

				.button-text {
					color: white;
					font-size: 1.5rem;
					user-select: none;
					margin-top: .25rem;
					transition: all .5s ease;
					font-family: "rivian", "aileron-bold";
				}

				border-radius: 6vh;
				transition: all .5s ease;
				border: 2px solid white;
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
  font-family: 'aileron';
  src: url('../../font/Rudder.otf');
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

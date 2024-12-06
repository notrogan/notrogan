<script setup lang="ts">
import { IonGrid, IonRow, IonCol } from '@ionic/vue';


</script>

<template>
    <div class="wrapper">
        <div class="text-wrapper">
            <div class="header">
                Meet the lineup
            </div>
            <div class="subheader">
                There's something for everyone. Choose the best build for you.
            </div>
        </div>
    </div>
</template>

<style scoped>

.wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
}

.header {
    text-align: center;
    margin-top: 6rem;
    font-size: 4.5rem;
    font-family: "rivian";
    color: black;
}

.subheader {
    text-align: center;
    font-size: 2rem;
    font-family: "rivian";
    color: black;
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

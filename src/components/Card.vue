<template>
  <div class="card">
    <div class="flip-card">
      <div :class="['flip-card-inner', { flipped: isFlipped }]">
        <div class="flip-card-front">
          <div class="star-container">
            <img
              class="star star--1"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--2"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--3"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--4"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--5"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--6"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--7"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--8"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
          </div>
          <img
            class="flip-card-front__sweet-30"
            src="../assets/images/Titulo.png"
            alt="sweet 30"
          />
          <img
            class="flip-card-front__karen-child"
            src="../assets/images/Karen-v2.png"
            alt="karen child"
          />
        </div>
        <div class="flip-card-back">
          <div class="star-container">
            <img
              class="star star--1"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--3"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--5"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--6"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
            <img
              class="star star--7"
              src="../assets/images/Estrella.png"
              alt="decorative star"
            />
          </div>
          <h2 class="flip-card-back__title">
            Ya no tengo <b>13</b>...<br />pero aún bailo <b>Thriller</b
            ><br />como si los tuviera.<br /><b>¡Ven a mi Sweet 30!</b>
          </h2>
          <p class="flip-card-back__paragraph--color">Domingo 1.º de junio</p>
          <p class="flip-card-back__paragraph--text-white">
            7:00 p. m.<br /><small>(el lunes es festivo :p)</small>
          </p>
          <p class="flip-card-back__paragraph">
            <b>
              Casa de los Sueños,<br />Territorio Aurora Boreal<br />Apto. 1336,
              Torre 1
            </b>
          </p>
          <p class="flip-card-back__paragraph--color"><b>Dress code:</b></p>
          <p class="flip-card-back__paragraph--text-white">
            Inspírate en la película<br />"Si tuviera 30", saca tu lado<br />ochentero
            y ponle sabor.
          </p>
          <p class="flip-card-back__paragraph--color"><b>Aporte:</b></p>
          <p class="flip-card-back__paragraph--text-white">
            Bebidas alcohólicas para compartir ;)
          </p>
          <p class="flip-card-back__subtitle">
            "No es solo una fiesta, es una<br /><b>película</b>... y tú estás
            <b>invitado</b><br />
            al <b>reparto principal</b>."
          </p>
        </div>
      </div>
    </div>
    <button @click="toggleFlip" class="flip-button">
      {{ isFlipped ? "Ver portada" : "¡Estoy Listo!" }}
    </button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const isFlipped = ref(false);

const toggleFlip = () => {
  isFlipped.value = !isFlipped.value;
};
</script>
<style scoped>
.card {
  font-family: "Montserrat", sans-serif;
  font-size: 10px;
}
.flip-card {
  background-color: transparent;
  width: 266px;
  height: 473px;
  perspective: 1000px;
  font-family: sans-serif;
}

.flip-card:hover {
  filter: drop-shadow(0 0 1em #9fd8ffaa);
  transition: all 0.4s ease-in-out;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.flipped {
  transform: rotateY(180deg);
}

.flip-button {
  margin-top: 1rem;
  padding: 0.5rem 1rem;
  background-color: #856695;
  color: white;
  border: none;
  border-radius: 0.5rem;
  cursor: pointer;
  font-weight: bold;
  transition: background 0.3s ease;
  font-size: 14px;
  outline: none;
}

.flip-button:hover {
  background-color: #b59dd0;
  filter: drop-shadow(0 0 0.5em #ffffffd7);
}

.flip-card-front,
.flip-card-back {
  box-shadow: 0 8px 14px 0 rgba(0, 0, 0, 0.2);
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  border-radius: 0.5rem;
}

.flip-card-front {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url(../assets/images/Tarjeta-fondo.png);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  color: white;
  font-family: "Montserrat", sans-serif;
}

.flip-card-front__sweet-30 {
  filter: drop-shadow(0 0 0.5em #ffffffd7);
  width: 80%;
  margin-bottom: 6rem;
}

.flip-card-front__karen-child {
  width: 80%;
  position: absolute;
  bottom: 0px;
}

.flip-card-back {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #a7d78e;
  color: white;
  transform: rotateY(180deg);
  font-family: "Montserrat", sans-serif;
}

.flip-card-back__title {
  font-size: 16px;
  font-weight: bold;
  /* color: #6e3b41; */
  /* color: #a7d78e; */
  color: #856695;
  /* color: #b59dd0; */
  /* color: #8ddfef; */
  margin: 0;
}

.flip-card-back__title b {
  color: white;
  font-size: 18px;
  filter: drop-shadow(0 0 0.5em #ffffffd7);
}

.flip-card-back__title b:hover {
  text-decoration-line: underline;
  color: #b59dd0;
}
.flip-card-back__paragraph {
  font-size: 12px;
  /* color: #6e3b41; */
}

.flip-card-back__paragraph--color {
  margin-bottom: 0;
  font-size: 12px;
  color: #856695;
  font-weight: bold;
}
.flip-card-back__subtitle {
  color: #856695;
  font-size: 12px;
}
.flip-card-back__subtitle b {
  color: white;
  filter: drop-shadow(0 0 0.5em #ffffffd7);
}
.flip-card-back__subtitle b:hover {
  text-decoration-line: underline;
  color: #b59dd0;
}
.flip-card-back__paragraph--text-white {
  margin-top: 0;
  font-size: 12px;
  color: white;
}

.star {
  position: absolute;
  opacity: 0.8;
  animation: flash 3s infinite ease-in-out alternate;
}
.star-container {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  pointer-events: none; /* para que no bloqueen clics */
  z-index: 2;
}
.star--1 {
  top: 18px;
  left: 30px;
  width: 30px;
  animation-delay: 0s;
}

.star--2 {
  top: 55px;
  right: 40px;
  width: 40px;
  animation-delay: 0s;
}

.star--3 {
  bottom: 15px;
  left: 20px;
  width: 30px;
  animation-delay: 0s;
}

.star--4 {
  bottom: 40px;
  right: 18px;
  width: 40px;
  animation-delay: 0s;
}
.star--5 {
  top: 165px;
  right: 35px;
  width: 30px;
  transform: rotate(20deg);
  animation-delay: 0s;
}
.star--6 {
  bottom: 145px;
  right: 18px;
  width: 25px;
  animation-delay: 0s;
}
.star--7 {
  top: 200px;
  left: 16px;
  width: 30px;
  transform: rotate(261deg);
  animation-delay: 0s;
}
.star--8 {
  bottom: 145px;
  left: 18px;
  width: 20px;
  animation-delay: 0s;
}
@keyframes flash {
  0% {
    transform: scale(1) rotate(0deg);
    opacity: 0.5;
  }
  50% {
    transform: scale(1.2) rotate(10deg);
    opacity: 1;
  }
  100% {
    transform: scale(1) rotate(-10deg);
    opacity: 0.5;
  }
}
</style>

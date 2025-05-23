<script setup></script>

<template>
  <div class="flip-card">
    <div class="flip-card-inner">
      <div class="flip-card-front">
        <img
          class="flip-card-front__sweet-30"
          src="../assets/images/Titulo.png"
          alt="sweet-30"
        />
        <img
          class="flip-card-front__karen-child"
          src="../assets/images/Karen-v2.png"
          alt="karen-child"
        />
      </div>
      <div class="flip-card-back">
        <h2 class="flip-card-back__title">
          Ya no tengo 13...<br />pero aún bailo Thriller<br />como si los
          tuviera.<br /><b>¡Ven a mi Sweet 30!</b>
        </h2>
        <p class="flip-card-back__paragraph--color">Domingo 1.º de junio</p>
        <p class="flip-card-back__paragraph--text-white">7:00 p. m.<br /><small>(el lunes es festivo :p)</small></p>
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
        <p class="flip-card-back__paragraph--text-white">Bebidas alcohólicas para compartir ;)</p>
        <p class="flip-card-back__paragraph--text-white">
          "No es solo una fiesta, es una<br />película... y tú estás invitado<br />
          al reparto principal."
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
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

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
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
}

.flip-card-back__title {
  font-size: 16px;
  font-weight: bold;
  color: #6e3b41;
  /* color: #a7d78e; */
  /* color: #856695; */
  /* color: #b59dd0; */
  /* color: #8ddfef; */
  margin: 0;
}

.flip-card-back__paragraph {
  font-size: 12px;
  /* color: #6e3b41; */
}

.flip-card-back__paragraph--color {
  margin-bottom: 0;
  font-size: 12px;
  color: #6e3b41;
}

.flip-card-back__paragraph--text-white {
  margin-top: 0;
  font-size: 12px;
  color: white;
}

</style>

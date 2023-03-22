<template>
  <div class="clock">
    <span class="time">00:00:00</span>
  </div>
</template>

<script>
function clock() {
  setInterval(() => {
    const data = new Date()
    const horas = data.toLocaleTimeString('pt-BR')
    const spanTempo = document.querySelector('span.time')

    spanTempo.innerHTML = horas
  }, 1000)
}

clock()
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
* {
  margin: 0px;
  padding: 0px;
  font-family: 'Poppins', sans-serif;
}

body {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgb(12, 44, 53);
}

.clock {
  background-color: whitesmoke;
  padding: 20px;
  font-size: 6rem;
  border-radius: 15px;
  box-shadow: 3px 2px 20px 0px #00000054;
}

</style>

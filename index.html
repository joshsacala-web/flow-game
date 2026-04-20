<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>AFib Flow Control</title>

<style>
body {
  margin: 0;
  background: radial-gradient(circle, #0f172a, #020617);
  color: white;
  font-family: Arial, sans-serif;
  text-align: center;
}

h2 {
  margin-top: 20px;
}

#ui {
  position: absolute;
  top: 10px;
  width: 100%;
}

#stability {
  font-size: 18px;
}

#timer {
  margin-top: 5px;
}

canvas {
  display: block;
}

button {
  margin-top: 10px;
  padding: 10px 20px;
  border: none;
  background: #22c55e;
  color: black;
  border-radius: 8px;
  cursor: pointer;
}
</style>
</head>

<body>

<div id="ui">
  <h2>AFib Flow Control</h2>
  <div id="stability">Stability: 50%</div>
  <div id="timer">Time: 60s</div>
  <button onclick="start()">Start</button>
</div>

<canvas id="canvas"></canvas>

<script>
const canvas = document.getElementById("canvas");
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let particles = [];
let mouse = { x: canvas.width / 2, y: canvas.height / 2 };
let stability = 50;
let running = false;
let timeLeft = 60;
let timerInterval;

document.addEventListener("mousemove", e => {
  mouse.x = e.clientX;
  mouse.y = e.clientY;
});

document.addEventListener("touchmove", e => {
  mouse.x = e.touches[0].clientX;
  mouse.y = e.touches[0].clientY;
});

function createParticles() {
  particles = [];
  for (let i = 0; i < 120; i++) {
    particles.push({
      x: Math.random() * canvas.width,
      y: Math.random() * canvas.height,
      vx: 0,
      vy: 0
    });
  }
}

function updateParticles() {
  let movement = Math.abs(mouse.x - canvas.width/2) + Math.abs(mouse.y - canvas.height/2);

  if (movement < 200) {
    stability += 0.2;
  } else {
    stability -= 0.4;
  }

  stability = Math.max(0, Math.min(100, stability));

  document.getElementById("stability").innerText = "Stability: " + Math.floor(stability) + "%";

  particles.forEach(p => {
    let dx = mouse.x - p.x;
    let dy = mouse.y - p.y;

    p.vx += dx * 0.0005 * (stability / 100);
    p.vy += dy * 0.0005 * (stability / 100);

    p.vx *= 0.95;
    p.vy *= 0.95;

    p.x += p.vx;
    p.y += p.vy;

    ctx.beginPath();
    ctx.arc(p.x, p.y, 2, 0, Math.PI * 2);
    ctx.fillStyle = `rgba(100,200,255,${stability/100})`;
    ctx.fill();
  });
}

function loop() {
  if (!running) return;

  ctx.fillStyle = "rgba(2,6,23,0.2)";
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  updateParticles();

  requestAnimationFrame(loop);
}

function start() {
  if (running) return;

  running = true;
  stability = 50;
  timeLeft = 60;

  createParticles();

  timerInterval = setInterval(() => {
    timeLeft--;
    document.getElementById("timer").innerText = "Time: " + timeLeft + "s";

    if (timeLeft <= 0) {
      stop();
    }
  }, 1000);

  loop();
}

function stop() {
  running = false;
  clearInterval(timerInterval);

  document.getElementById("timer").innerText = "Done";
  document.getElementById("stability").innerText =
    "Final Stability: " + Math.floor(stability) + "%";
}
</script>

</body>
</html>

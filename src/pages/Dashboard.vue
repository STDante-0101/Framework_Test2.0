<template>
  <body>
    <div class="sign">
      <span class="fast-flicker">Fr</span>ame<span class="flicker">wor</span>k
    </div>
  </body>
</template>


<style scoped>
@font-face {
  font-family: Clip;
  src: url("https://acupoftee.github.io/fonts/Clip.ttf");
}

body {
  background-color: #141114;
  background-image: linear-gradient(335deg, black 23px, transparent 23px),
    linear-gradient(155deg, black 23px, transparent 23px),
    linear-gradient(335deg, black 23px, transparent 23px),
    linear-gradient(155deg, black 23px, transparent 23px);
  background-size: 78px 78px;
  background-position: 0px 2px, 4px 35px, 29px 31px, 34px 6px;
}

.sign {
  position: absolute;
  display: flex;
  width: 50%;
  height: 50%;
  background-image: radial-gradient(
    ellipse 50% 35% at 50% 50%,
    #6b1839,
    transparent
  );
  transform: translate(-70%, -50%);
  letter-spacing: 2;
  left: 50%;
  top: 50%;
  font-family: "Clip";
  text-transform: uppercase;
  font-size: 8em;
  color: #ffe6ff;
  text-shadow: 0 0 0.6rem #ffe6ff, 0 0 1.5rem #aa0de7,
    -0.2rem 0.1rem 1rem #aa0de7, 0.2rem 0.1rem 1rem #aa0de7,
    0 -0.5rem 2rem #aa0de7, 0 0.5rem 3rem #aa0de7;
  animation: shine 2s forwards, flicker 3s infinite;
}

@keyframes blink {
  0%,
  22%,
  36%,
  75% {
    color: #ffe6ff;
    text-shadow: 0 0 0.6rem #ffe6ff, 0 0 1.5rem #8005e4,
      -0.2rem 0.1rem 1rem #ac03d6d2, 0.2rem 0.1rem 1rem #8a06d6,
      0 -0.5rem 2rem #8804bd, 0 0.5rem 3rem hsl(288, 92%, 36%);
  }
  28%,
  33% {
    color: #aa0de7;
    text-shadow: none;
  }
  82%,
  97% {
    color: #aa0de7;
    text-shadow: none;
  }
}

.flicker {
  animation: shine 2s forwards, blink 3s 2s infinite;
}

.fast-flicker {
  animation: shine 2s forwards, blink 10s 1s infinite;
}

@keyframes shine {
  0% {
    color: #6b1839;
    text-shadow: none;
  }
  100% {
    color: #ffe6ff;
    text-shadow: 0 0 0.6rem #ffe6ff, 0 0 1.5rem #aa0de7,
      -0.2rem 0.1rem 1rem #aa0de7, 0.2rem 0.1rem 1rem #aa0de7,
      0 -0.5rem 2rem #aa0de7, 0 0.5rem 3rem #aa0de7;
  }
}

@keyframes flicker {
  from {
    opacity: 1;
  }

  4% {
    opacity: 0.9;
  }

  6% {
    opacity: 0.85;
  }

  8% {
    opacity: 0.95;
  }

  10% {
    opacity: 0.9;
  }

  11% {
    opacity: 0.922;
  }

  12% {
    opacity: 0.9;
  }

  14% {
    opacity: 0.95;
  }

  16% {
    opacity: 0.98;
  }

  17% {
    opacity: 0.9;
  }

  19% {
    opacity: 0.93;
  }

  20% {
    opacity: 0.99;
  }

  24% {
    opacity: 1;
  }

  26% {
    opacity: 0.94;
  }

  28% {
    opacity: 0.98;
  }

  37% {
    opacity: 0.93;
  }

  38% {
    opacity: 0.5;
  }

  39% {
    opacity: 0.96;
  }

  42% {
    opacity: 1;
  }

  44% {
    opacity: 0.97;
  }

  46% {
    opacity: 0.94;
  }

  56% {
    opacity: 0.9;
  }

  58% {
    opacity: 0.9;
  }

  60% {
    opacity: 0.99;
  }

  68% {
    opacity: 1;
  }

  70% {
    opacity: 0.9;
  }

  72% {
    opacity: 0.95;
  }

  93% {
    opacity: 0.93;
  }

  95% {
    opacity: 0.95;
  }

  97% {
    opacity: 0.93;
  }

  to {
    opacity: 1;
  }
}

</style>
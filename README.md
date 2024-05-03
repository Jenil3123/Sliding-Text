<style>
:root {
  --fontSize: calc(5vw + 5vh);
  --duration: 15s;
}

@media screen and (orientation: portrait) {
  :root {
    --fontSize: calc(1vw + 7vh);
    font-family: fantasy;
  }
}

@media screen and (max-height: 600px) {
  :root {
    --fontSize: calc(2vw + 2vh);
    font-family: fantasy;
  }
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

*::selection{
  background-color: darkgreen;
}

body {
  font-family: "Inter", sans-serif;
}

.xray {
  background-color: #ffffff;
}

.xray__wrapper {
  height: 30vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow: hidden;
}

.xray__content {
  display: flex;
}

.xray__line {
  font-size: var(--fontSize);
  line-height: 1em;
  text-transform: uppercase;
  flex-shrink: 0;
  flex-basis: 100%;
  white-space: nowrap;
  mix-blend-mode: exclusion;
  color: white;
}

.xray__line:nth-child(1) {
  padding-right: 0.5ch;
}

.top {
  animation: moveLeft var(--duration) linear infinite;
  font-family: fantasy;
}

.bottom-line {
  animation: moveRight var(--duration) linear infinite;
  font-family: fantasy;
}

@keyframes moveRight {
  from {
    transform: translateX(-100%) matrix(-1, 0, 0, 1, 0, 0);
  }

  to {
    transform: translateX(0) matrix(-1, 0, 0, 1, 0, 0);
  }
}
  @keyframes moveLeft {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-100%);
  }
}

{% comment %} This is not Dynamic section {% endcomment %}
  
</style>

<div class="xray">
  <div class="xray__wrapper">
    <div class="xray__content">
      <p class="xray__line top">Sliding &nbsp;&nbsp;  Text &nbsp;&nbsp; </p>
      <p class="xray__line top">Sliding &nbsp;&nbsp;  Text &nbsp;&nbsp; </p>
    </div>
    <div class="xray__content">
      <p class="xray__line bottom-line">Sliding &nbsp;&nbsp;  Text &nbsp;&nbsp; </p>
      <p class="xray__line bottom-line">Sliding &nbsp;&nbsp;  Text &nbsp;&nbsp; </p>
    </div>
  </div>
</div>


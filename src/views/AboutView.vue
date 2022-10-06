<template>
  <div class="about">
    <h1>This is an about emojis page</h1>
    <ul class="emojis">
      <li>👍</li>
      <li>❤️</li>
      <li>😴</li>
      <li>😍</li>
      <li>✌️</li>
      <li>🏀</li>
    </ul>

    <!-- <svg viewBox="0 0 300 162"> -->
    <filter id="mix">
      <feGaussianBlur in="SourceGraphic" result="blur" stdDeviation="5" />
      <feColorMatrix
        in="blur"
        mode="matrix"
        values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 60 -36"
      />
    </filter>

    <g filter="url(#mix)">
      <rect width="300" height="50" x="0" y="50" rx="25" fill="#e3e3e3" />
      <circle cx="40" cy="75" fill="#e3e3e3" id="pop" />
    </g>
    <!-- </svg> -->
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  methods: {},
};
</script>

<style lang="scss">
// body {}

.emojis {
  list-style: none;
  margin: 0;
  padding: 0;
  width: 600px;

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

  padding: 0 20px;
  box-sizing: border-box;
  display: flex;
}

.emojis li {
  flex: 1;
  font-size: 60px;
  text-align: center;
  transition: 0.2s all ease-in-out;
}

.emojis li:hover {
  transform: scale(1.6);
}

.emojis + svg #pop {
  r: 20px;
  transition: 0.2s r ease-in-out;
}

.emojis:hover + svg #pop {
  r: 40px;
}
</style>

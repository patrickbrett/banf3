<template>
  <div>
    <nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Questrial', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.content-full,
.content-split {
  width: 80vw;
  max-width: 1600px;
  margin: 40px auto;
  text-align: justify;
}

.content-split {
  display: flex;
  justify-content: space-between;
}

.content-split-1,
.content-split-2 {
  width: 45%;
}

.content-full p,
.content-split p {
  margin: 1em 0;
}

@media screen and (max-width: 1000px) {
  .content-split {
    flex-direction: column;
  }

  .content-split-1,
  .content-split-2 {
    width: 100%;
  }
}
</style>

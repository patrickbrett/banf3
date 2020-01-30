<template>
  <section id="testimonial">
    <img :src="require('@/assets/img/testimonial.png')" alt="Testimonial" />
  </section>
</template>

<script>
export default {}
</script>

<style>
  #testimonial {
    display: flex;
    justify-content: center;
    padding-top: 80px;
  }

  #testimonial img {
    width: 30vw;
    min-width: 600px;
  }

  @media screen and (max-width: 600px) {
    #testimonial img {
      width: 90vw;
      min-width: 0;
    }
  }
</style>

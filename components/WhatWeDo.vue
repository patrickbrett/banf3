<template>
<section class="content-full" id="what-we-do">
  <div>
    <h2>What We Do</h2>
    <div class="service-list">
      <div class="service-item">
        <nuxt-link to="/services/picture-framing">
          <img :src="require('@/assets/img/gallery-1.jpg')" />
          <h4>Picture Framing</h4>
        </nuxt-link>
      </div>
      <div class="service-item">
        <nuxt-link to="/services/custom-frames">
          <img :src="require('@/assets/img/gallery-1.jpg')" />
          <h4>Custom Frames</h4>
        </nuxt-link>
      </div>
      <div class="service-item">
        <nuxt-link to="/services/canvas-stretching">
          <img :src="require('@/assets/img/gallery-1.jpg')" />
          <h4>Canvas Stretching</h4>
        </nuxt-link>
      </div>
    </div>
  </div>
</section>
</template>

<script>
export default {}
</script>

<style>
.content-full {
  width: 80vw;
  max-width: 1600px;
  margin: 0 auto;
}

#what-we-do {
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
  padding-top: 80px;
  padding-bottom: 80px;
}
.service-list {
  display: flex;
  margin: 20px 0;
}

.service-item {
  background: #fff;
  border: 4px solid #A9815E;
  margin-right: 20px;
  transition: all 0.4s;
}

.service-item:hover {
  box-shadow: 0 5px 20px 0 rgba(0, 0, 0, 0.3);
  transform: translateY(-4px);
}

.service-item a {
  color: #000;
  text-decoration: none;
  padding: 20px;
  display: block;
}

.service-item img {
  width: 200px;
}

@media screen and (max-width: 1000px) {
  .service-list {
    flex-direction: column;
    align-items: flex-start;
  }

  .service-item {
    margin: 20px 0;
  }
}
</style>

<template>
  <header>
    <section id="pre-nav">
      <img
        id="logo"
        :src="require('@/assets/img/logo.png')"
        alt="Bentleigh Art 'n' Frame logo"
      />
      <nav id="nav-mobile" :class="isNavOpen ? 'active' : ''">
        <img
          id="mobile-nav-button"
          :src="require('@/assets/icon/nav.svg')"
          @click="toggleNavOpen"
        />
        <ul>
          <li><nuxt-link to="/" exact>Home</nuxt-link></li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
          <li><nuxt-link to="/gallery">Gallery</nuxt-link></li>
          <li class="list-inner-container">
            <nuxt-link to="/services">Services</nuxt-link>
            <ul class="list-inner">
              <li>
                <nuxt-link to="/services/picture-framing"
                  >Picture Framing</nuxt-link
                >
              </li>
              <li>
                <nuxt-link to="/services/custom-frames"
                  >Custom Frames</nuxt-link
                >
              </li>
              <li>
                <nuxt-link to="/services/canvas-stretching"
                  >Canvas Stretching</nuxt-link
                >
              </li>
            </ul>
          </li>
          <li><nuxt-link to="/contact">Contact</nuxt-link></li>
        </ul>
        <!--<div id="mobile-nav-marker">about</div>-->
      </nav>
      <div id="pre-nav-contact">
        <div>
          <img :src="require('@/assets/icon/phone.svg')" /><span
            ><a href="tel:03-9557-4268">(03) 9557 4268</a></span
          >
        </div>
        <div>
          <img :src="require('@/assets/icon/map.svg')" /><span
            >343 Centre Rd, Bentleigh VIC 3204</span
          >
        </div>
      </div>
      <div id="pre-nav-social">
        <a
          v-if="General['show-facebook']"
          :href="General['facebook-page-url']"
          target="_blank"
          rel="noopener"
          ><img :src="require('@/assets/icon/facebook.svg')"
        /></a>
        <a
          v-if="General['show-instagram']"
          :href="General['instagram-page-url']"
          target="_blank"
          rel="noopener"
          ><img :src="require('@/assets/icon/instagram.svg')"
        /></a>
      </div>
    </section>
    <nav id="nav-main">
      <ul>
        <li><nuxt-link to="/" exact>Home</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
        <li><nuxt-link to="/gallery">Gallery</nuxt-link></li>
        <li class="list-inner-container">
          <nuxt-link to="/services">Services</nuxt-link>
          <ul class="list-inner">
            <li>
              <nuxt-link to="/services/picture-framing"
                >Picture Framing</nuxt-link
              >
            </li>
            <li>
              <nuxt-link to="/services/custom-frames">Custom Frames</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/services/canvas-stretching"
                >Canvas Stretching</nuxt-link
              >
            </li>
          </ul>
        </li>
        <li><nuxt-link to="/contact">Contact</nuxt-link></li>
      </ul>
    </nav>
    <section v-if="showGallery" id="header-gallery">
      <transition name="slide">
        <img
          :key="i"
          :alt="`Header photo ${i}`"
          v-for="i of Array.from(Array(maxGallery).keys())"
          v-if="gallery === i"
          class="gallery-img"
          :src="require(`@/assets/img/gallery-${i + 1}.jpg`)"
        />
      </transition>
    </section>
  </header>
</template>

<script>
import General from '../assets/content/general/general.json'

export default {
  data() {
    return {
      isNavOpen: false,
      General,
      gallery: 1,
      maxGallery: 4
    }
  },
  methods: {
    toggleNavOpen() {
      this.isNavOpen = !this.isNavOpen
    },
    nextGallery() {
      this.gallery = (this.gallery + 1) % this.maxGallery
    }
  },
  created() {
    setInterval(this.nextGallery, General['gallery-transition-seconds'] * 1000)
  },
  props: {
    showGallery: {
      type: Boolean,
      default: false,
      required: false
    }
  }
}
</script>

<style>
#pre-nav {
  display: flex;
  width: 80vw;
  max-width: 1600px;
  margin: 40px auto;
  justify-content: flex-end;
  align-items: center;
}

#logo {
  height: 200px;
  margin-right: auto;
}

#pre-nav-contact {
  margin-right: 80px;
}

#pre-nav-contact div {
  display: flex;
  align-items: center;
  margin: 20px 0;
}

#pre-nav-contact a {
  text-decoration: none;
  color: #000;
  font-weight: bold;
}

#pre-nav-contact img {
  width: 30px;
  margin-right: 20px;
}

#pre-nav-social a {
  margin-left: 10px;
}

#pre-nav-social a:hover {
  opacity: 0.7;
  transition: 0.4s opacity;
}

#pre-nav-social img {
  width: 50px;
}

#nav-main {
  background: #5d4937;
  height: 60px;
  color: #fff;
  text-transform: lowercase;
  display: flex;
  align-items: center;
}

#nav-main > ul {
  list-style-type: none;
  width: 80vw;
  max-width: 1600px;
  margin: 0 auto;
  padding: 0;
  height: 100%;
}

#nav-main > ul > li {
  display: inline-block;
  cursor: pointer;
  height: 100%;
  padding: 0;
}

#nav-main > ul > li a {
  padding: 0 20px;
  height: 100%;
  display: flex;
  align-items: center;
}

#nav-mobile {
  display: none;
}

li a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
}

#nav-main > ul > li:hover {
  background: rgba(255, 255, 255, 0.3);
}

#nav-main .list-inner-container {
  position: relative;
  justify-self: flex-start;
}

#nav-main .list-inner {
  list-style-type: none;
  display: block;
  position: absolute;
  top: 60px;
  left: 0;
  background: #fff;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.3);
  padding: 0;
  margin: 0;
  max-height: 0;
  overflow: hidden;
  transition: all 1s;
  z-index: 5;
}

#nav-main .list-inner li {
  white-space: nowrap;
}

#nav-main ul.list-inner > li a {
  display: block;
  padding: 20px;
  color: #000;
}

.list-inner li:hover {
  background: #eee;
}

#nav-main li:hover .list-inner {
  display: block;
  max-height: 400px;
  opacity: 1;
}

.gallery-img {
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
}

@media screen and (max-width: 1000px) {
  #pre-nav {
    flex-direction: column;
  }

  #pre-nav-contact {
    margin: 20px 0;
  }

  #nav-main {
    display: none;
  }

  #mobile-nav-button {
    height: 30px;
    margin-top: 15px;
    margin-bottom: 15px;
    margin-left: 20px;
  }

  #nav-mobile {
    background: #5d4937;
    height: auto;
    color: #fff;
    text-transform: lowercase;
    display: flex;
    align-items: flex-start;
    max-height: 60px;
    transition: 0.4s all;
    overflow: hidden;
    margin-top: 20px;
  }

  #nav-mobile.active {
    max-height: 1000px;
  }

  #nav-mobile > ul {
    list-style-type: none;
    width: 80vw;
    max-width: 1600px;
    margin: 0 auto;
    padding: 0;
    height: 100%;
  }

  #nav-mobile > ul > li {
    display: block;
    cursor: pointer;
    height: auto;
    padding: 0;
    opacity: 0;
    transition: 0.4s all;
  }

  #nav-mobile.active > ul > li {
    opacity: 1;
  }

  #nav-mobile > ul > li a {
    padding: 0 20px;
    display: flex;
    align-items: center;
  }

  li a {
    color: #fff;
    text-decoration: none;
    height: 60px;
    font-weight: bold;
  }

  #nav-mobile > ul > li:hover {
    background: rgba(255, 255, 255, 0.3);
  }

  #nav-mobile .list-inner-container {
    position: relative;
    justify-self: flex-start;
    height: auto;
  }

  #nav-mobile .list-inner {
    list-style-type: none;
    padding: 0;
    margin: 0;
  }

  #nav-mobile .list-inner li {
    padding: 0 20px;
    white-space: nowrap;
  }

  .list-inner li a {
    color: #fff;
  }

  .list-inner li:hover {
    background: rgba(255, 255, 255, 0.3);
  }

  #mobile-nav-marker {
    align-self: center;
    margin-right: auto;
    margin-left: 0;
    opacity: 1;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.slide-enter-active {
  transition: transform 1s ease-out;
}

.slide-leave-active {
  transition: transform 1s ease-in, opacity 1s;
}

.slide-enter {
  /*opacity: 0;*/
  transform: translateX(100vw);
}

.slide-leave-to {
  opacity: 0;
  transform: scale(0.7);
}

#header-gallery {
  height: calc(100vw * 1089 / 2560);
  position: relative;
  background: #000;
  z-index: 1;
}
</style>

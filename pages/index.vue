<template>
  <div class="container">
    <site-header show-gallery />
    <div id="text-content">
      <section class="content-split">
        <div class="content-split-1">
          <h2>Welcome!</h2>
          <p>
            Bentleigh Art ’n’ Frame is a family-owned framing shop that has been
            serving the local community since 2011.
          </p>
          <p>
            We pride ourselves on the highest quality service at great prices. If
            you’re tired of second-rate framing, come in and have a chat about
            what our personal, professional service can do for you!
          </p>
        </div>
        <div class="content-split-2">
          <h2>About Us</h2>
          <p>
            Bentleigh Art ’n’ Frame is a family business through and through. We
            use only the highest quality materials and assemble our custom frames
            in house.
          </p>
          <p>
            Our family has run local businesses in the
            Bentleigh and McKinnon area since moving here in 2001. We are members of the Picture Framers’ Guild of Australia.
          </p>

          <p>
            We work hard, but take a break from time to time to support the
            Bentleigh Arts Festival and other community initiatives.
          </p>
        </div>
      </section>
      <what-we-do />
      <testimonial />
    </div>
    <site-footer />
  </div>
</template>

<script>
import Header from '../components/Header'
import Footer from '../components/Footer'
import WhatWeDo from '../components/WhatWeDo'
import Testimonial from '../components/Testimonial'

export default {
  components: {
    siteHeader: Header,
    siteFooter: Footer,
    whatWeDo: WhatWeDo,
    testimonial: Testimonial
  },
  head () {
    return {
      title: "Bentleigh Art 'n' Frame"
    }
  }
}
</script>

<style>
</style>

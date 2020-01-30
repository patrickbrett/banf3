<template>
  <div class="container">
    <site-header />
    <div id="text-content">
      <section class="content-split">
        <div class="content-full">
          <h1>Contact</h1>
          <p>
            Work in progress - check back soon!
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
      title: "Contact | Bentleigh Art 'n' Frame"
    }
  }
}
</script>

<style>
</style>

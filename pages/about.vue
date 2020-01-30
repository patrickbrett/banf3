<template>
  <div class="container">
    <site-header />
    <div id="text-content">
      <section class="content-split">
        <div class="content-full" v-html="parseMarkdown(Content['about']['content-1'])">
        </div>
      </section>
      <what-we-do />
      <testimonial />
    </div>
    <site-footer />
  </div>
</template>

<script>
import { markdown } from 'markdown'

import Header from '../components/Header'
import Footer from '../components/Footer'
import WhatWeDo from '../components/WhatWeDo'
import Testimonial from '../components/Testimonial'

import Content from '@/assets/content/pages/pages.json'

export default {
  components: {
    siteHeader: Header,
    siteFooter: Footer,
    whatWeDo: WhatWeDo,
    testimonial: Testimonial
  },
  methods: {
    parseMarkdown (content) {
      return markdown.toHTML(content)
    }
  },
  head () {
    return {
      title: "About | Bentleigh Art 'n' Frame"
    }
  },
  data () {
    return {
      Content
    }
  }
}
</script>

<style>
</style>

<template>
  <footer>
    <div id="footer-main">
      <div>
        <h3>Find Us</h3>
        <p>Bentleigh Art 'n' Frame</p>
        <p>{{ General['address'] }}</p>
      </div>
      <div>
        <h3>Contact Us</h3>
        <p>{{ General['phone-number'] }}</p>
        <p>{{ General['email'] }}</p>
      </div>
      <div>
        <h3>Open Hours</h3>
        <div v-html="parseMarkdown(General['open-hours'])"></div>
      </div>
    </div>
    <div id="footer-copyright">
      &copy; 2020 Bentleigh Art 'n' Frame. Site by
      <a href="https://bellcurve.com.au" target="_blank" rel="noopener"
        >Bellcurve</a
      >.
    </div>
  </footer>
</template>

<script>
import { markdown } from 'markdown'

import General from '@/assets/content/general/general.json'

export default {
  methods: {
    parseMarkdown(content) {
      return markdown.toHTML(content)
    }
  },
  data() {
    return {
      General
    }
  }
}
</script>

<style>
footer {
  /*background: #5D4937;*/
  background-color: #7c644e;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='20' height='12' viewBox='0 0 20 12'%3E%3Cg fill-rule='evenodd'%3E%3Cg id='charlie-brown' fill='%235d4937' fill-opacity='0.4'%3E%3Cpath d='M9.8 12L0 2.2V.8l10 10 10-10v1.4L10.2 12h-.4zm-4 0L0 6.2V4.8L7.2 12H5.8zm8.4 0L20 6.2V4.8L12.8 12h1.4zM9.8 0l.2.2.2-.2h-.4zm-4 0L10 4.2 14.2 0h-1.4L10 2.8 7.2 0H5.8z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
  color: #fff;

  margin-top: 80px;
  padding-top: 160px;
  clip-path: polygon(0 25%, 50% 0, 100% 25%, 100% 100%, 0 100%);

  width: 100vw;
}

#footer-main {
  display: flex;
  width: 80vw;
  max-width: 1600px;
  margin: 0 auto;
  justify-content: space-between;
}

#footer-copyright {
  text-align: center;
  border-top: 1px solid rgba(255, 255, 255, 0.4);
  width: 80vw;
  max-width: 1600px;
  margin: 160px auto 0;
  padding-top: 40px;
  padding-bottom: 20px;
}

#footer-copyright a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
}

@media screen and (max-width: 1000px) {
  #footer-main {
    flex-direction: column;
  }

  #footer-main div {
    margin-top: 40px;
  }

  #footer-copyright {
    margin-top: 80px;
  }

  footer {
    clip-path: polygon(0 10%, 50% 0, 100% 10%, 100% 100%, 0 100%);
    margin-top: 40px;
    padding-top: 80px;
  }
}
</style>

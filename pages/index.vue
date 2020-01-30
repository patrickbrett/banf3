<template>
  <div class="container">
    <header>
      <section id="pre-nav">
        <img
          id="logo"
          :src="require('@/assets/img/logo.png')"
           alt="Bentleigh Art 'n' Frame logo"
        />
        <div id="pre-nav-contact">
          <div><img :src="require('@/assets/icon/phone.svg')" /><span>9557 4268</span></div>
          <div>
            <img :src="require('@/assets/icon/map.svg')" /><span>343 Centre Rd,
            Bentleigh VIC 3204</span>
          </div>
        </div>
        <div id="pre-nav-social">
          <img :src="require('@/assets/icon/facebook.svg')" />
          <img :src="require('@/assets/icon/instagram.svg')" />
        </div>
      </section>
      <nav id="nav-main">
        <ul>
          <li>Home</li>
          <li>About</li>
          <li>Gallery</li>
          <li class="list-inner-container">
            Services
            <ul class="list-inner">
              <li>Picture Framing</li>
              <li>Custom Frames</li>
              <li>Canvas Stretching</li>
            </ul>
          </li>
          <li>Contact</li>
        </ul>
      </nav>
      <section id="header-gallery">
        <img class="gallery-img" :src="require('@/assets/img/gallery-1.jpg')" />
      </section>
    </header>
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
            Kim and the rest of the family have run local businesses in the
            Bentleigh and McKinnon area since we moved here in 2001.
          </p>

          <p>We are members of the Picture Framers’ Guild of Australia.</p>

          <p>
            We work hard, but take a break from time to time to support the
            Bentleigh Arts Festival and other community initiatives.
          </p>
        </div>
      </section>
      <section class="content-full" id="what-we-do">
        <div>
          <h2>What We Do</h2>
          <div class="service-list">
            <div class="service-item">
              <img :src="require('@/assets/img/gallery-1.jpg')" />
              <h4>Picture Framing</h4>
            </div>
            <div class="service-item">
              <img :src="require('@/assets/img/gallery-1.jpg')" />
              <h4>Custom Frames</h4>
            </div>
            <div class="service-item">
              <img :src="require('@/assets/img/gallery-1.jpg')" />
              <h4>Canvas Stretching</h4>
            </div>
          </div>
        </div>
      </section>
      <section id="testimonial">
        <img :src="require('@/assets/img/testimonial.png')" alt="Testimonial" />
      </section>
    </div>
    <footer>
      <div id="footer-main">
        <div>
          <h3>Find Us</h3>
          <p>Bentleigh Art 'n' Frame</p>
          <p>343 Centre Rd</p>
          <p>Bentleigh, VIC 3204</p>
        </div>
        <div>
          <h3>Contact Us</h3>
          <p>(03) 9557 4268</p>
          <p>info@bentleighartnframe.com.au</p>
        </div>
        <div>
          <h3>Open Hours</h3>
          <p>Mon-Fri: 10am - 5pm</p>
          <p>Sat: 10am - 3pm</p>
          <p>Closed Sun and public holidays</p>
        </div>
      </div>
      <div id="footer-copyright">
        &copy; 2020 Bentleigh Art 'n' Frame. Site by <a href="https://bellcurve.com.au" target="_blank" rel="noopener">Bellcurve</a>.
      </div>
    </footer>
  </div>
</template>

<script>
export default {}
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

  #pre-nav-contact {
    margin-right: 40px;
  }

  #pre-nav-contact div {
    display: flex;
    align-items: center;
    margin: 20px 0;
  }

  #pre-nav-contact img {
    width: 30px;
    margin-right: 20px;
  }

  #logo {
    height: 200px;
    margin-right: auto;
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
}

#nav-main > ul > li {
  display: inline-block;
  margin: 0 40px 0 0;
}

#nav-main .list-inner-container {
  position: relative;
}

#nav-main .list-inner {
  list-style-type: none;
  display: none;
  position: absolute;
  background: #fff;
  color: #000;
  padding: 0;
  margin: 0;
}

#nav-main .list-inner li {
  margin: 20px;
  white-space: nowrap;
}

#nav-main li:hover .list-inner {
  display: block;
}

.gallery-img {
  width: 100vw;
}

.content-full {
  width: 80vw;
  max-width: 1600px;
  margin: 0 auto;
}

.content-split {
  display: flex;
  width: 80vw;
  max-width: 1600px;
  margin: 40px auto;
  text-align: justify;
  justify-content: space-between;
}

  .content-split-1 {
    width: 50%;
  }

  .content-split-2 {
    width: 50%;
  }

  .content-split p {
    margin: 1em 0;
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
    padding: 20px;
    margin-right: 20px;
  }

  .service-item img {
    width: 200px;
  }

  #testimonial {
    display: flex;
    justify-content: center;
    padding-top: 80px;
  }

  #testimonial img {
    width: 30vw;
  }

  footer {
    background: #5D4937;
    color: #fff;

    margin-top: 80px;
    padding-top: 160px;
    clip-path: polygon(
      0 25%,
      50% 0,
      100% 25%,
      100% 100%,
      0 100%
    );

    /*position: absolute;*/
    /*bottom: 0;*/
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
</style>

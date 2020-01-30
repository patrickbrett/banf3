<template>
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
</template>

<script>
export default {}
</script>

<style>
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
      clip-path: polygon(
        0 10%,
        50% 0,
        100% 10%,
        100% 100%,
        0 100%
      );
      margin-top: 40px;
      padding-top: 80px;
    }
  }
</style>

<script>
  import Grid from './Grid.svelte'
  export let background = 'rgba(82, 98, 125, 0.8)'
  export let color = 'white'
  export let height = ''

  const date = new Date().getFullYear()

  const scrollToTop = () => {
    document.body.scrollTop = 0 // For Safari
    document.documentElement.scrollTop = 0 // For Chrome, Firefox, IE and Opera
  }
</script>

<footer style="height:{height};background:{background};color:{color};">
  <div>
    <Grid columns="1fr 1fr 1fr" gap="2em">
      <div>
        <div>
          <h4>Contact Information</h4>
          <p>
            <i class="fas fa-envelope" />
            <a href="mailto:info@fischerimaging.com" target="_blank"
              >info@fischerimaging.com</a
            >
          </p>
          <p>
            <i class="fas fa-address-card" />
            <a href="https://goo.gl/maps/mrCeZyKE76Ao5aSe9" target="_blank"
              >600 17th Street, Suite 2800<br />
              South, Denver CO 80202, USA</a
            >
          </p>
          <p>
            <i class="fab fa-linkedin" />
            <a
              href="https://www.linkedin.com/company/fischer-imaging"
              target="_blank">Linkedin Profile</a
            >
          </p>
        </div>
      </div>
      <div>
        <div>
          <h4>Latest News</h4>
          <a
            href="https://sbir.cancer.gov/programseducation/icorps"
            target="_blank"
          >
            <p>
              Fischer Imaging awarded NIH grant and spot in I-Corps™ at NIH 2020
            </p>
          </a>
          <p>January 10, 2020</p>
        </div>
        <div>
          <a href="https://www.medtechstrategist.com/sf-2019" target="_blank">
            <p>
              Fischer Imaging will present at the MedTech Strategist Innovation
              Summit San Francisco 2019 on November 18-19, 2019 in Burlingame,
              California
            </p>
          </a>
          <p>July 9th, 2019</p>
        </div>
      </div>

      <div class="badges">
        <img src="/images/biocom.png" alt="biocom" />
        <img src="/images/launchpad.png" alt="launchpad" />
      </div>
    </Grid>
  </div>
  <slot />
</footer>
<div class="bottom">
  <div>
    <p>© {date} Fischer Imaging. All rights reserved.</p>
    <p><a href="/" on:click|preventDefault={scrollToTop}>Back To Top</a></p>
  </div>
</div>

<style>
  footer {
    margin: auto;
    padding: 1.5rem;
    color: white;
    text-align: center;
  }
  div {
    max-width: 960px;
    margin: 0 auto 2em;
  }
  h4 {
    padding-bottom: 1em;
    border-bottom: 1px solid white;
    text-transform: uppercase;
  }
  a {
    color: white;
  }
  p {
    line-height: 1.5;
  }
  footer div div {
    margin-top: 2em;
  }
  footer div div p,
  h4 {
    text-align: left;
  }
  p {
    margin-top: 1em;
    text-align: center;
  }
  .badges {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2em;
  }
  .badges img {
    max-width: 200px;
  }
  .badges img:first-child {
    background: white;
  }
  .bottom {
    position: relative;
    max-width: 100%;
    background-color: #323942;
  }
  .bottom div {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 960px;
  }
  .bottom p {
    margin-top: 0;
    margin-bottom: 0;
    padding: 2em;
    color: white;
  }
</style>

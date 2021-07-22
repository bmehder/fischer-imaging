<script>
  import Header from './Layouts/Header.svelte'
  import Section from './Layouts/Section.svelte'
  import Grid from './Layouts/Grid.svelte'
  import Hero from './Hero.svelte'
  import About from './About.svelte'
  import Questions from './Questions.svelte'
  import Products from './Products.svelte'
  import Statement from './Statement.svelte'
  import News from './News.svelte'
  import Contact from './Contact.svelte'
  import Footer from './Layouts/Footer.svelte'
</script>

<Header />
<main>
  <Hero />
  <div id="about-us">
    <Section padding="2em 2em 4em" background="#f1f1f1" title="About Us">
      <Grid columns="2fr 1fr" gap="4em">
        <About />
      </Grid>
    </Section>
  </div>

  <Section padding="2em" background="white" title="Any Questions?">
    <Questions />
  </Section>

  <div id="products">
    <Section padding="2em 2em 4em" background="#f1f1f1" title="Products">
      <Grid columns="2fr 1fr" gap="4em">
        <Products
          src="/images/products-1-fischer-imaging.jpg"
          alt="Products 1 - Fischer Imaging"
        >
          <h3 slot="title">
            <span>MammoSOUND</span> Fusion mammography-ultrasound imaging
          </h3>
          <p>
            MammoSOUND, based on our proprietary technology combines automated
            breast ultrasound with digital mammography allowing both imaging
            modalities in the same patient encounter and configuration for
            improved and efficient breast cancer screening and diagnosis.
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Modi
            veritatis repellat sapiente dolores illum quod et ullam rem alias ut
            explicabo soluta odio, rerum maxime? Sit rem asperiores magni
            voluptas quaerat officiis sint libero, deserunt, reiciendis
            inventore ut. Vel aliquid quam dolore reprehenderit quae?
          </p>
        </Products>
        <Products
          src="/images/products-2-fischer-imaging.jpg"
          alt="Products 2 - Fischer Imaging"
        >
          <h3 slot="title">
            <span>MammoCAT</span> Digital Mammography & Tomosynthesis
          </h3>
          <p>
            MammoCAT is based on our proprietary slot scanning technology which
            doubles the resolution higher contrast and resolution (up to 25
            microns) and increases the contrast of today’s mammography using
            less than half the radiation dose without requiring painful breast
            compression. MammoCAT does not require the use of an anti-scatter
            grid. MammoCAT will perform both planar digital mammography and
            digital breast tomosynthesis.
          </p>
        </Products>
        <Products
          src="/images/products-3-fischer-imaging.jpg"
          alt="Products 3 - Fischer Imaging"
        >
          <h3 slot="title">
            <span>Mammo360</span> Full 360° 3D Computed Tomography of the breast
          </h3>
          <p>
            Mammo360 uses the same imaging gantry as MammoCAT to and perform
            3-dimensional CT imaging of the breast. The patient lies in a
            comfortable, prone position and her breast is imaged without
            compression. Mammo360 will allow screening, diagnosis and
            stereotactic biopsy all in one system. This multi-purpose use will
            improve equipment utilization, hospital workflow and reduce demands
            on space.
          </p>
        </Products>
      </Grid>
      <p style="margin-top: 2em;">
        <em
          >*All of the above listed products are currently under development and
          are not available for sale at this time.</em
        >
      </p>
    </Section>
  </div>

  <Section background="rgba(82, 98, 125, 0.8)">
    <Statement />
  </Section>

  <div id="news-events">
    <Section margin="4em 0" background="white" title="News & Events">
      <News />
    </Section>
  </div>

  <div id="contact-us">
    <Section padding="2em 2em 4em" background="#f1f1f1" title="Contact Us">
      <Contact />
    </Section>
  </div>
</main>
<Footer />

<style>
  main {
    text-align: center;
    padding: 0;
    padding-bottom: 0;
    margin: 0 auto;
    font-size: 16px;
    line-height: 1.5em;
  }
  h3 span {
    color: #227ad2;
  }
</style>

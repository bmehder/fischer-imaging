<script>
  import Grid from './Layouts/Grid.svelte'
</script>

<div>
  <Grid columns="1fr 1fr" gap="2em">
    <aside>
      <p>
        <a href="https://medtechstrategist.com/sf-2019" target="_blank"
          >Fischer Imaging will present at the MedTech Strategist Innovation
          Summit San Francisco 2019 on November 18-19, 2019 in Burlingame,
          California</a
        >
      </p>
      <p>Date: July 9, 2019</p>
    </aside>
    <aside>
      <p>
        <a
          href="https://sbir.cancer.gov/programseducation/icorps"
          target="_blank"
          >Fischer Imaging awarded NIH grant and spot in I-CorpsTM at NIH 2020</a
        >
      </p>
      <p>Date: June 10, 2020</p>
    </aside>
    <aside>
      <p>
        <a
          href="https://www.airmeet.com/e/7538af00-ca22-11eb-9d3b-191ee3a4adb8"
          target="_blank"
          >Fischer Imaging to present at AngelMD Pitch Club on Tuesday, June 22,
          2021</a
        >
      </p>
      <p>Date: June 22, 2021</p>
    </aside>
  </Grid>
</div>

<style>
  aside {
    padding: 2em;
    text-align: left;
    background: #f1f1f1;
    border: 4px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.24);
    transition: all 300ms;
  }
  aside:hover {
    background-color: #227ad2;
    color: white;
  }
  aside:hover a {
    color: white;
  }
  p:first-child {
    font-weight: bold;
  }
</style>

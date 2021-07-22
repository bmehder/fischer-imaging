<script>
  import { onMount } from 'svelte'
  import { fly } from 'svelte/transition'
  let onLoad = false
  onMount(() => (onLoad = true))
</script>

<section>
  <img class="hero" src="/images/slider-fischer-imaging.jpg" alt="Hero" />
  {#if onLoad}
    <div>
      <p in:fly={{ delay: 1000, duration: 600, x: 500, opacity: 0 }}>
        Radiation doses equivalent to current FFDM systems
      </p>

      <p in:fly={{ delay: 2500, duration: 600, x: 500, opacity: 0 }}>
        Elimination of breast compression during screening
      </p>

      <p in:fly={{ delay: 4000, duration: 600, x: 500, opacity: 0 }}>
        True 3D Computed Tomography imaging
      </p>

      <p in:fly={{ delay: 5500, duration: 600, x: 500, opacity: 0 }}>
        25 micron image resolution
      </p>
    </div>
  {/if}
</section>

<style>
  section {
    position: relative;
    text-align: left;
    padding-top: 50%;
  }
  div {
    position: absolute;
    top: 42%;
    right: 10%;
    font-size: 1.5vw;
    color: #0e345a;
    text-align: right;
    font-weight: 500;
    letter-spacing: 2px;
  }
  p {
    line-height: initial;
  }
  img {
    display: block;
    position: absolute;
    top: 0px;
    width: 100%;
    height: 100%;
  }
  @media screen and (max-width: 640px) {
    section div {
      display: none;
    }
  }
</style>

<script>
  export let boxed = false
  export let title = false
  export let margin = ''
  export let padding = ''
  export let background = ''
  export let color = ''
  export let titleColor = '#001515'
  export let align = 'center'
</script>

<section
  class:boxed
  style="background:{background};color:{color};margin:{margin};padding:{padding};"
>
  <div class="content-wrap">
    {#if title}
      <h3 style="color:{titleColor};text-align:{align};">{title}</h3>
    {/if}
    <slot />
  </div>
</section>

<style>
  .boxed {
    max-width: 960px;
    margin: auto;
  }
  .content-wrap {
    max-width: 960px;
    margin: auto;
    /* padding: 2em; */
  }
  h3 {
    margin: 1em auto;
    text-align: center;
    font-size: 2.5em;
    line-height: 1em;
    color: #227ad2;
  }
  @media screen and (max-width: 640px) {
    section {
      padding: 1em 2em !important;
    }
    h3 {
      font-size: 1.5em;
    }
  }
</style>

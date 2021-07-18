<script>
  export let src = ''
  export let alt = ''
</script>

<div>
  <slot name="title" />
  <slot />
</div>
<div>
  <img {src} {alt} />
</div>

<style>
  div {
    text-align: left;
  }
  img {
    display: block;
    max-width: 400px;
    margin: 2em auto;
    border-radius: 4px;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.24);
  }
  @media screen and (max-width: 640px) {
    img {
      max-width: 300px;
      margin-bottom: 4em;
    }
  }
</style>

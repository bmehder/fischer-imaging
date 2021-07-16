<script>
  import Flex from './Flex.svelte'
  export let sticky = false
  export let uppercase = false
  export let background = 'white'
  export let color = '#001515'

  let mobile = false
  const showMobile = () => {
    mobile = !mobile
  }
</script>

<header class:sticky style="background:{background};color:{color};">
  <nav class="main">
    <a href="/"
      ><img
        class="logo"
        src="/images/logo-fischer-imaging.png"
        alt="Fischer Imaging Logo"
      /></a
    >
    <ul class:uppercase>
      <li><a href="/">Home</a></li>
      <li><a href="#about-us">About Us</a></li>
      <li><a href="#products">Products</a></li>
      <li>
        <a href="#news-events">News & Events</a>
      </li>
      <li><a href="#contact-us">Contact Us</a></li>
    </ul>
  </nav>
  <nav class="mobile">
    <Flex justify="space-between">
      <a href="/"
        ><img
          class="logo-mobile"
          src="/images/logo-fischer-imaging.png"
          alt="Fischer Imaging Logo"
        /></a
      >
      <div class="bun">
        <div on:click={showMobile} class="hamburger">&#9776;</div>
      </div>
    </Flex>
    {#if mobile}
      <a href="/"
        ><img
          class="logo"
          src="/images/logo-fischer-imaging.png"
          alt="Fischer Imaging Logo"
        /></a
      >
      <ul class:uppercase class="mobile">
        <li>
          <a on:click={showMobile} href="/">Home</a>
        </li>
        <li><a href="#about-us">About Us</a></li>
        <li><a href="#products">Products</a></li>
        <li>
          <a on:click={showMobile} href="#news-events">News & Events</a>
        </li>
        <li>
          <a on:click={showMobile} href="#contact-us">Contact Us</a>
        </li>
      </ul>
    {/if}
  </nav>
</header>

<style>
  header {
    position: fixed;
    width: 100%;
    padding: 3em 0;
    background: darkorange;
    color: #001515;
    text-align: center;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.25);
  }
  .sticky {
    position: fixed;
    z-index: 100;
  }
  .logo {
    display: block;
    width: 300px;
    height: auto;
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1020px;
    margin: 0 auto;
    padding: 0 1em;
  }
  nav ul {
    display: flex;
    justify-content: space-between;
  }
  nav ul li {
    list-style-type: none;
    padding: 0 1rem;
    font-weight: 600;
  }
  nav ul li:last-child {
    padding-right: 0;
  }
  nav ul li a {
    height: auto;
    color: #001515;
    text-decoration: none;
  }
  nav ul li a:hover {
    padding-bottom: 1em;
    color: #227ad2;
    border-bottom: 4px solid white;
  }
  .uppercase {
    text-transform: uppercase;
  }
  ul.mobile {
    width: 100%;
    flex-direction: column;
    margin: 0;
    text-align: center;
  }
  nav div {
    display: flex;
    justify-content: space-between;
  }
  .logo-mobile {
    display: block;
    width: 120px;
  }
  ul.mobile li {
    padding: 1em 0;
  }
  .bun {
    align-items: center;
  }
  .hamburger {
    font-size: 3em;
    /* padding-right: 0.5em; */
  }
  .hamburger,
  nav.mobile {
    display: none;
  }
  @media screen and (max-width: 640px) {
    header {
      padding: 1em;
    }
    nav.main {
      display: none;
    }
    nav.mobile {
      display: block;
    }
    .hamburger {
      display: block;
    }
  }
</style>

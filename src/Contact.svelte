<script>
  const form_id = ''
</script>

<div>
  <p>
    We are available by e-mail. You can also use our quick contact form to ask a
    question about our services that we regularly provide.
  </p>
  <form action="https://formspree.io/f/{form_id}">
    <input name="name" type="text" placeholder="Your Name" required />
    <input name="_replyto" type="email" placeholder="Your Email" required />
    <input name="phone" type="phone" placeholder="Your Phone" />
    <input name="subject" type="text" placeholder="Your Subject" required />
    <textarea name="message" placeholder="Your Message" required />
    <button type="submit">Send Message</button>
  </form>
</div>

<style>
  form,
  p {
    width: 400px;
    margin: auto;
    text-align: left;
  }
  input,
  textarea,
  button {
    display: block;
    width: 100%;
    margin: 1em auto;
    padding: 1em;
    border-radius: 4px;
  }
  textarea {
    min-height: 200px;
  }
  button {
    background: #227ad2;
    color: white;
    font-weight: bold;
    transition: all 300ms;
  }
  button:hover {
    background: hsl(210, 72%, 38%);
  }
  @media screen and (max-width: 640px) {
    form,
    p {
      width: 100%;
    }
  }
</style>

---
layout: default
title: Contact
permalink: /contact/
---

<div class="contact-wrapper">

  <p class="contact-intro">
    For enquiries regarding publications, rights, or general correspondence,
    please use the form below.
  </p>

  <form name="contact"
        method="POST"
        data-netlify="true"
        netlify-honeypot="bot-field"
        action="/contact/thank-you/"
        class="contact-form">

    <input type="hidden" name="form-name" value="contact">

    <p class="hidden">
      <label>Don’t fill this out:
        <input name="bot-field">
      </label>
    </p>

    <div class="field">
      <label for="name">Name</label>
      <input type="text" id="name" name="name" required>
    </div>

    <div class="field">
      <label for="email">Email</label>
      <input type="email" id="email" name="email" required>
    </div>

    <div class="field">
      <label for="message">Message</label>
      <textarea id="message" name="message" rows="6" required></textarea>
    </div>

    <button type="submit" class="contact-submit">
      Send message
    </button>

  </form>

</div>
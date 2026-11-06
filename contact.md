---
layout: contact
title: "Contact & Support - 67Runner"
description: Contact and support for 67Runner.
permalink: /contact/
---

# Contact &amp; Support

Use this form for technical support, purchase issues, or privacy and data requests about 67Runner.

Apple and Google handle refunds for purchases made through their stores. Use this form for game-related purchase delivery issues or other support questions.

<form id="contact-form" class="contact-form" action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="2b263805-55f2-499e-a51e-209e6ef6c119">
    <input type="hidden" name="subject" value="67Runner support request">
    <input type="hidden" name="from_name" value="67Runner website">

    <div class="form-row">
        <div class="form-field">
            <label for="contact-name">Name <span class="form-optional">(optional)</span></label>
            <input id="contact-name" name="name" type="text" autocomplete="name">
        </div>

        <div class="form-field">
            <label for="contact-email">Email address</label>
            <input id="contact-email" name="email" type="email" autocomplete="email" required>
        </div>
    </div>

    <div class="form-field">
        <label for="contact-topic">Topic</label>
        <select id="contact-topic" name="topic" required>
            <option value="" selected disabled>Select a topic</option>
            <option value="technical-support">Technical support</option>
            <option value="purchase-issue">Purchase issue</option>
            <option value="privacy-or-data-request">Privacy or data request</option>
            <option value="other">Other</option>
        </select>
    </div>

    <div class="form-field">
        <label for="contact-message">Message</label>
        <p id="contact-message-help" class="form-field-hint">For technical issues, include your device model, operating-system version, game version, and a description of what happened. Do not include passwords or payment-card details.</p>
        <textarea id="contact-message" name="message" rows="14" aria-describedby="contact-message-help" required></textarea>
    </div>

    <div class="h-captcha" data-captcha="true" data-lang="en" data-theme="dark"></div>
    <p id="captcha-error" class="form-error" role="alert" tabindex="-1" hidden>Please complete the captcha before submitting the form.</p>

    <button type="submit" class="form-submit">Send message</button>

    <p class="form-privacy-note">
        We use the information you submit to respond to your request. Web3Forms processes the submission on our behalf, and hCaptcha helps protect the form from abuse. See the <a href="{{ '/privacy/' | relative_url }}">Privacy Policy</a> for information about personal-data handling and your rights.
    </p>
</form>

<script>
    const contactForm = document.getElementById('contact-form');
    const captchaError = document.getElementById('captcha-error');

    contactForm.addEventListener('submit', event => {
        const captchaResponse = contactForm.querySelector('textarea[name="h-captcha-response"]');

        if (!captchaResponse || !captchaResponse.value) {
            event.preventDefault();
            captchaError.hidden = false;
            captchaError.focus();
        } else {
            captchaError.hidden = true;
        }
    });
</script>
<script src="https://web3forms.com/client/script.js" async defer></script>

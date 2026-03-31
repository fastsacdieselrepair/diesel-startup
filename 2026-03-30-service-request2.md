---
layout: post
title: "Service Request"
date: 2026-03-30 03:59:01 +0000
---

<p>Please fill out the form below to submit your service request:</p>

<form action="https://web3forms.com/api/v1/email" method="POST">
    <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
    <input type="text" name="name" placeholder="Your Name" required>
    <input type="email" name="email" placeholder="Your Email" required>
    <textarea name="message" placeholder="Your Service Request" required></textarea>
    <button type="submit">Submit</button>
</form>

<div id="form-message"></div>

<script>
    const form = document.querySelector('form');
    form.onsubmit = async (e) => {
        e.preventDefault();
        const formData = new FormData(form);
        const response = await fetch(form.action, {
            method: 'POST',
            body: formData,
        });
        const result = await response.json();
        document.getElementById('form-message').innerText = result.message;
    };
</script>
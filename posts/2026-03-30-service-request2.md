---
layout: default
title: Fast Sac Diesel Repair
---

<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #000;
    color: #fff;
  }

  header {
    background: linear-gradient(90deg, #000, #111);
    padding: 20px;
    border-bottom: 3px solid orange;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .branding {
    display: flex;
    align-items: center;
    gap: 15px;
  }

  .logo {
    width: 60px;
    height: 60px;
    background-color: orange;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    color: black;
    font-size: 20px;
  }

  .brand-text h1 {
    margin: 0;
    color: orange;
    font-size: 24px;
  }

  .brand-text p {
    margin: 0;
    font-size: 12px;
    color: #ccc;
  }

  .contact a {
    color: #fff;
    text-decoration: none;
    margin-left: 15px;
    font-size: 14px;
  }

  .contact a:hover {
    color: orange;
  }

  .hero {
    text-align: center;
    padding: 40px 20px;
    background: url('{{ "/assets/images/diesel-truck.jpg" | relative_url }}') center/cover no-repeat;
    border-bottom: 3px solid orange;
  }

  .hero h2 {
    font-size: 32px;
    margin: 0;
    color: #fff;
    text-shadow: 0 0 10px rgba(0,0,0,0.8);
  }

  .hero p {
    margin-top: 10px;
    color: #ddd;
    text-shadow: 0 0 5px rgba(0,0,0,0.8);
  }

  .container {
    max-width: 600px;
    margin: 40px auto;
    padding: 20px;
    background-color: #111;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(255, 165, 0, 0.3);
  }

  label {
    display: block;
    margin-top: 15px;
    color: orange;
  }

  input, textarea {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
    border: none;
    border-radius: 5px;
    background-color: #222;
    color: #fff;
  }

  textarea {
    height: 150px;
    resize: vertical;
  }

  button {
    margin-top: 20px;
    width: 100%;
    padding: 15px;
    background-color: orange;
    color: #000;
    font-size: 16px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: 0.3s;
  }

  button:hover {
    background-color: #ff8c00;
    transform: scale(1.02);
  }

  footer {
    text-align: center;
    padding: 20px;
    border-top: 2px solid #222;
    color: #777;
    font-size: 12px;
  }
</style>

<header>
  <div class="branding">
    <div class="logo">FS</div>
    <div class="brand-text">
      <h1>Fast Sac Diesel Repair</h1>
      <p>Heavy Duty • Mobile Service • Reliable Repairs</p>
    </div>
  </div>
  <div class="contact">
    <a href="mailto:fastsacrepair@gmail.com">Email</a>
    <a href="tel:19165727890">(916) 572-7890</a>
  </div>
</header>

<section class="hero">
  <h2>Diesel Truck Repair You Can Count On</h2>
  <p>Fast response. Honest work. Sacramento’s trusted diesel repair service.</p>
</section>

<div class="container">
  <h2>Request Service</h2>
  <form onsubmit="sendEmail(); return false;">

    <label for="name">Name</label>
    <input type="text" id="name" required>

    <label for="phone">Phone Number</label>
    <input type="tel" id="phone" required>

    <label for="vehicle">Vehicle Year, Make, Model</label>
    <input type="text" id="vehicle" required>

    <label for="service">Service Requested</label>
    <textarea id="service" required></textarea>

    <button type="submit">Submit Request</button>

  </form>
</div>

<footer>
  © {{ site.time | date: '%Y' }} Fast Sac Diesel Repair • Serving Sacramento & Surrounding Areas
</footer>

<script>
  function sendEmail() {
    const name = document.getElementById('name').value;
    const phone = document.getElementById('phone').value;
    const vehicle = document.getElementById('vehicle').value;
    const service = document.getElementById('service').value;

    const subject = encodeURIComponent('Diesel Repair Service Request');
    const body = encodeURIComponent(
      'Name: ' + name + '\n' +
      'Phone: ' + phone + '\n' +
      'Vehicle: ' + vehicle + '\n\n' +
      'Service Requested:\n' + service
    );

    window.location.href = `mailto:fastsacrepair@gmail.com?subject=${subject}&body=${body}`;
  }
</script>

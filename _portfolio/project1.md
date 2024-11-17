<style>
  .container {
    max-width: 90% !important; /* Overrides any other width settings */
    margin: 0 auto;
  }
</style>

---
title: "Bio-Inspired Propeller Analysis"
excerpt: "3D model analysis of propeller with bio-inspired Leading Edge Tubercules.<br/><img src='/images/propeller1_thumbnail.jpg'>"
collection: portfolio
---

<style>
  .project-container {
    display: grid;
    grid-template-columns: 1fr 1fr; /* Two equal columns */
    gap: 20px;
    margin-top: 20px;
  }
  .project-image {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
  }
  .project-text {
    padding: 10px;
  }
  .project-title {
    font-weight: bold;
    margin-bottom: 10px;
  }
</style>

<div class="project-container">
  <!-- Text Section -->
  <div class="project-text">
    <div class="project-title">What?</div>
    <p>3D model a baseline small (10x4.7) 2-blade propeller and a modified propeller with bio-inspired Leading Edge Tubercules to experimentally analyze performance (Cp, Ct).</p>

    <div class="project-title">How?</div>
    <ul>
      <li>Used surface modeling features in CATIA V5 to design the propellers ready to be 3D printed.</li>
      <li>Assembled a test rig with a beam-type strain gauge to measure thrust and monitor motor power feed and prop RPM using an Arduino controller.</li>
      <li>Performed static thrust wind tunnel experiments up to 5000 RPM.</li>
    </ul>

    <div class="project-title">Results</div>
    <ul>
      <li>Reduced power requirement by 21% for lower RPMs and by 7% for higher RPMs at less than 5% thrust penalty.</li>
      <li>Built relationships with rapid prototyping manufacturers.</li>
    </ul>
  </div>

  <!-- Image Section -->
  <div>
    <img src="/images/propeller1_full.jpg" alt="Baseline Propeller" class="project-image">
  </div>
</div>

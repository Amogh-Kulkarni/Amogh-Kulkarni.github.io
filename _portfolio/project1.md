---
title: "Bio-Inspired Propeller Analysis"
excerpt: "3D model analysis of propeller with bio-inspired Leading Edge Tubercules.<br/><img src='/images/propeller1_thumbnail.jpg' alt='Bio-Inspired Propeller Thumbnail'>"
collection: portfolio
---

<style>
  .subpart-container {
    margin-top: 20px;
  }
  .content-row {
    display: grid;
    grid-template-columns: 1fr; /* Single column for stacked text and images */
    gap: 20px;
    align-items: center;
    margin-bottom: 20px;
  }
  .content-text {
    padding: 10px;
  }
  .content-image {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    margin-top: 10px;
  }
  .content-title {
    font-weight: bold;
    margin-bottom: 10px;
  }
  .content-images {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Responsive grid for images */
    gap: 15px; /* Space between images */
  }

  /* Optional: Adjust image grid on larger screens */
  /* Uncomment the following if you want to control the number of columns on larger screens */
  /*
  @media (min-width: 768px) {
    .content-images {
      grid-template-columns: repeat(2, 1fr); /* Two columns */
    }
  }
  */
</style>

This project involves the 3D modeling and experimental analysis of a baseline small (10x4.7) 2-blade propeller and a modified propeller featuring bio-inspired Leading Edge Tubercules. The objective is to analyze and compare the performance metrics, specifically the power coefficient (Cp) and thrust coefficient (Ct), between the baseline and modified designs.

## Bio-Inspired Leading Edge Tubercules

### Overview:
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section for What, How, and Results -->
    <div class="content-text">
      <div class="content-title">What?</div>
      <p>3D model a baseline small (10x4.7) 2-blade propeller and a modified propeller with bio-inspired Leading Edge Tubercules to experimentally analyze performance (Cp, Ct).</p>

      <div class="content-title">How?</div>
      <ul>
        <li>Used surface modeling features in CATIA V5 to design the propellers ready to be 3D printed.</li>
        <li>Assembled a test rig with a beam-type strain gauge to measure thrust and monitor motor power feed and prop RPM using an Arduino controller.</li>
        <li>Performed static thrust wind tunnel experiments up to 5000 RPM.</li>
      </ul>

      <div class="content-title">Results</div>
      <ul>
        <li>Reduced power requirement by 21% for lower RPMs and by 7% for higher RPMs at less than 5% thrust penalty.</li>
        <li>Built relationships with rapid prototyping manufacturers.</li>
      </ul>
    </div>

    <!-- Image Section for What, How, and Results -->
    <div class="content-images">
      <img src="/images/propeller1_full.jpg" alt="Baseline Propeller" class="content-image">
      <img src="/images/propeller1_modified.jpg" alt="Modified Propeller with Tubercules" class="content-image">
    </div>
  </div>
</div>

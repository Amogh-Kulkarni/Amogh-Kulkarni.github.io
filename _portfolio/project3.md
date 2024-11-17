---
title: "Advanced Aerodynamics: Wing Design"
excerpt: "Designing an aircraft wing for transonic flow with an elliptical lift distribution using Excel, VBA, and VORLAX.<br/><img src='/images/wing_design_thumbnail.jpg'>"
collection: portfolio
---

<style>
  .subpart-container {
    margin-top: 20px;
  }
  .content-row {
    display: grid;
    grid-template-columns: 2fr; /* Default to a single column layout */
    gap: 20px;
    align-items: start;
    margin-bottom: 20px;
  }
  .content-text {
    padding: 10px;
  }
  .content-images-right {
    display: grid;
    grid-template-columns: 1fr 1fr; /* Text on left, images on right */
    gap: 20px;
    align-items: start;
  }
  .content-images-below {
    display: flex;
    flex-direction: column;
    gap: 10px;
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
</style>


This project involves designing an aircraft wing to meet specific structural, aerodynamic, and flight condition requirements for subcritical flow at the critical Mach number. The goal was to achieve an elliptical lift distribution while considering transonic effects and various design parameters.

## Overview:
<div class="subpart-container">
  <!-- You can switch between content-images-right and content-images-below based on the desired layout -->
  <div class="content-images-right">
    <!-- Text Section for What and How -->
    <div class="content-text">
      <div class="content-title">What?</div>
      <ul>
        <li>Design an aircraft wing for a set of given structural and specified transonic regime and flight condition.</li>
        <li>Design the wing for subcritical flow at critical Mach number to fit an elliptical lift distribution.</li>
      </ul>

      <div class="content-title">How?</div>
      <ul>
        <li>Used Excel and VBA to create a custom-designed wing by varying wing thickness, camber line, sweep, taper ratio, and twist to produce VORLAX input files.</li>
        <li>Used VORLAX to determine aerodynamic qualities and utilized MATLAB scripts for postprocessing the results.</li>
      </ul>
    </div>

    <!-- Image Section for What and How -->
    <div class="content-images-below">
      <img src="/images/wing_design_1.jpg" alt="Selected Wing Design" class="content-image">
      <img src="/images/wing_design_2.jpg" alt="Wing Sections" class="content-image">
      <img src="/images/wing_design_3.jpg" alt="Lift Distribution" class="content-image">
      <img src="/images/wing_design_4.jpg" alt="Pressure Distribution" class="content-image">
    </div>
  </div>
</div>

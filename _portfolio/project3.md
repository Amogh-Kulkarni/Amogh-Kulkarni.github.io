---
title: "Advanced Aerodynamics: Wing Design"
excerpt: "Designing an aircraft wing for transonic flow with an elliptical lift distribution using Excel, VBA, and VORLAX.<br/><img src='/images/wing_design_thumbnail.jpg' alt='Wing Design Thumbnail'>"
collection: portfolio
---

<style>
  .subpart-container {
    margin-top: 20px;
  }
  .content-row {
    display: grid;
    grid-template-columns: 2fr; /* Single column for stacked text and images */
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
    /* Removed font-size to maintain uniformity */
  }
</style>

Designing an aircraft wing for transonic flow with an elliptical lift distribution is a complex task that involves various computational and analytical methods. This project leverages Excel, VBA, and VORLAX to achieve an optimal wing design that balances aerodynamic efficiency and structural integrity.

### Overview:
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section for What, How, and Results -->
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

      <div class="content-title">Results</div>
      <ul>
        <li>Developed an agile workflow to conceptualise wing design for specific design lift and transverse distribution.</li>
        <li>Designed Sub sritical no-shock wing for transonic application</li>
      </ul>
    </div>

    <!-- Image Section for What, How, and Results -->
    <div>
      <img src="/images/wing_design_1.jpg" alt="Selected Wing Design" class="content-image">
      <img src="/images/wing_design_2.jpg" alt="Wing Sections" class="content-image">
      <img src="/images/wing_design_3.jpg" alt="Lift Distribution" class="content-image">
      <img src="/images/wing_design_4.jpg" alt="Pressure Distribution" class="content-image">
    </div>
  </div>
</div>

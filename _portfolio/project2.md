---
title: "Wave Drag Reduction Analysis"
excerpt: "Study wave drag reduction by varying the leading edge shape of cascade fins in supersonic flow.<br/><img src='/images/cascade_fins_thumbnail.jpg' alt='Cascade Fins Thumbnail'>"
collection: portfolio
---

<style>
  .subpart-container {
    margin-top: 20px;
  }
  .content-row {
    display: grid;
    grid-template-columns: 2fr; /* Single column for stacked images */
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
</style>


This project aims to study wave drag reduction by varying the leading edge shape of cascade fins in a supersonic flow regime. Below, we present the key subparts of the project, detailing each aspect of the analysis and its outcomes.


### Overview:
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section for What, How, and Results -->
    <div class="content-text">
      <div class="content-title">What?</div>
      <p>Study wave drag reduction by varying the leading edge shape of cascade fins in a supersonic flow regime.</p>

      <div class="content-title">How?</div>
      <ul>
        <li>Used CATIA V5 to design baseline and modified cascade fins.</li>
        <li>Conducted a benchmarking process of the CFD model by validating results in subsonic and supersonic regimes with established previous works.</li>
        <li>Ran multiple simulations at M=2 with varied leading edge shapes to study drag coefficient (Cd).</li>
      </ul>

      <div class="content-title">Results</div>
      <ul>
        <li>Implemented Fluent script with an established workflow to reduce preprocessing times.</li>
        <li>15° Sharp leading edge displayed overall better performance and low drag with a weaker shock wave.</li>
      </ul>
    </div>

    <!-- Image Section for What, How, and Results -->
    <div>
      <img src="/images/cascade_fins_full.jpg" alt="Cascade Fins Full View" class="content-image">
      <img src="/images/cascade_fins_simulation.jpg" alt="Cascade Fins Simulation" class="content-image">
    </div>
  </div>
</div>

---
title: "Wave Drag Reduction Analysis"
excerpt: "Study wave drag reduction by varying the leading edge shape of cascade fins in supersonic flow.<br/><img src='/images/cascade_fins_thumbnail.jpg'>"
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
    <p>Study wave drag reduction by varying the leading edge shape of cascade fins in a supersonic flow regime.</p>

    <div class="project-title">How?</div>
    <ul>
      <li>Used CATIA V5 to design baseline and modified cascade fins.</li>
      <li>Conducted a benchmarking process of the CFD model by validating results in subsonic and supersonic regimes with established previous works.</li>
      <li>Ran multiple simulations at M=2 with varied leading edge shapes to study drag coefficient (Cd).</li>
    </ul>

    <div class="project-title">Results</div>
    <ul>
      <li>Implemented Fluent script with an established workflow to reduce preprocessing times.</li>
      <li>15° Sharp leading edge displayed overall better performance and low drag with a weaker shock wave.</li>
    </ul>
  </div>

  <!-- Image Section -->
  <div>
    <img src="/images/cascade_fins_full.jpg" alt="Cascade Fins" class="project-image">
  </div>
</div>

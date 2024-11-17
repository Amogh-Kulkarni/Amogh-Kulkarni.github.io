---
title: "Wave Drag Reduction Analysis"
excerpt: "Study wave drag reduction by varying the leading edge shape of cascade fins in supersonic flow.<br/><img src='/images/cascade_fins_thumbnail.jpg' alt='Cascade Fins Thumbnail'>"
collection: portfolio
---

<style>
  /* Reset some basic elements for consistency */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  /* Ensure body takes full height and prevents horizontal overflow */
  body, html {
    width: 100%;
    height: 100%;
    overflow-x: hidden;
    font-family: Arial, sans-serif; /* Set a default font */
    line-height: 1.6; /* Improve readability */
    color: #333; /* Set a default text color */
  }

  /* Container for overall content */
  .container {
    max-width: 1200px; /* Maximum width of the content */
    width: 90%; /* Responsive width */
    margin: 0 auto; /* Centers the container horizontally */
    padding: 20px 0; /* Top and bottom padding */
  }

  /* Styling for the main title */
  .container h1 {
    font-size: 2.5em; /* Increased font size for prominence */
    margin-bottom: 20px; /* Space below the title */
    text-align: center; /* Center the title */
  }

  /* Container for each subpart */
  .subpart-container {
    margin-top: 30px; /* Adjusted for better separation */
  }

  /* Grid layout for content rows */
  .content-row {
    display: flex;
    flex-direction: column; /* Stack text and images vertically */
    gap: 20px;
    margin-bottom: 30px; /* Space below each content row */
  }

  /* Styling for the text section */
  .content-text {
    padding: 10px;
  }

  /* Styling for the images section */
  .content-images {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Responsive grid */
    gap: 15px; /* Space between images */
  }

  .content-image {
    width: 100%; /* Ensures each image fills the container's width */
    height: auto;
    border-radius: 8px;
    object-fit: cover; /* Ensures images cover the container without distortion */
  }

  .content-title {
    font-weight: bold;
    margin-bottom: 10px;
    font-size: 1.2em; /* Increased for better readability */
  }

  /* Responsive Design for Medium Screens */
  @media (max-width: 992px) {
    .container {
      width: 95%; /* Slightly wider on medium screens */
    }
  }

  /* Responsive Design for Small Screens */
  @media (max-width: 576px) {
    .container {
      width: 100%; /* Full width on very small screens */
      padding: 10px 0; /* Reduced padding */
    }

    .container h1 {
      font-size: 2em; /* Adjust font size for small screens */
      margin-bottom: 15px; /* Adjust margin below title */
    }

    .content-title {
      font-size: 1em; /* Adjust font size for small screens */
    }
  }
</style>

<div class="container">
  # Wave Drag Reduction Analysis

  This project focuses on studying wave drag reduction by varying the leading edge shape of cascade fins in a supersonic flow regime. The objective is to optimize the fin design to minimize drag while maintaining aerodynamic efficiency.

  ## Overview:
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
      <div class="content-images">
        <img src="/images/cascade_fins_full.jpg" alt="Cascade Fins Full View" class="content-image">
        <img src="/images/cascade_fins_simulation.jpg" alt="Cascade Fins Simulation" class="content-image">
      </div>
    </div>
  </div>
</div>

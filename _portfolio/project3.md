---
title: "Advanced Aerodynamics: Wing Design"
excerpt: "Designing an aircraft wing for transonic flow with an elliptical lift distribution using Excel, VBA, and VORLAX.<br/><img src='/images/wing_design_thumbnail.jpg' alt='Wing Design Thumbnail'>"
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
    display: grid;
    grid-template-columns: 1fr; /* Single column layout */
    gap: 20px;
    align-items: start; /* Align items to the top */
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

Designing an aircraft wing for transonic flow with an elliptical lift distribution is a complex task that involves various computational and analytical methods. This project leverages Excel, VBA, and VORLAX to achieve an optimal wing design that balances aerodynamic efficiency and structural integrity.

  ## Overview:
  <div class="subpart-container">
    <div class="content-row">
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
      <div class="content-images">
        <img src="/images/wing_design_1.jpg" alt="Selected Wing Design" class="content-image">
        <img src="/images/wing_design_2.jpg" alt="Wing Sections" class="content-image">
        <img src="/images/wing_design_3.jpg" alt="Lift Distribution" class="content-image">
        <img src="/images/wing_design_4.jpg" alt="Pressure Distribution" class="content-image">
      </div>
    </div>
  </div>
</div>

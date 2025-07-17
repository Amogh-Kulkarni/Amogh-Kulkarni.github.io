---
title: "Data-Driven Recovery of Relativistic Corrections in Black Hole Dynamics"
excerpt: "Leveraging SciML and neural network-enhanced UDEs in Julia to capture relativistic effects in black hole orbits and gravitational waveform predictions.<br/><img src='/images/black_hole_model_thumbnail.jpg'>"
collection: portfolio
---

<style>
  .subpart-container {
    margin-top: 20px;
  }
  .content-row {
    display: grid;
    grid-template-columns: 2fr; /* Two columns: text and images */
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

## 1. Introduction and Motivation

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <p>
        Modeling black hole dynamics in strong gravitational fields requires capturing relativistic corrections that go beyond classical Newtonian physics. This project leverages SciML tools in Julia to develop a Universal Differential Equation (UDE) framework enhanced with neural networks. Our approach aims to recover these relativistic effects in orbital mechanics and gravitational waveforms, providing a data-driven correction to traditional models.
      </p>
    </div>
    <div>
      <img src="/images/black_hole_intro.jpg" alt="Black Hole Dynamics Overview" class="content-image">
    </div>
  </div>
</div>

## 2. Methodology

### 2.1 Orbital Models

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Classical & Relativistic Models</div>
      <ul>
        <li><strong>Newtonian Orbit Model:</strong> Simulates orbital motion using classical mechanics.</li>
        <li><strong>Relativistic Orbit Model:</strong> Incorporates Schwarzschild corrections to capture strong gravity effects.</li>
      </ul>
      <p>
        These models serve as benchmarks to assess the effectiveness of our neural network-enhanced model.
      </p>
    </div>
    <div>
      <img src="/images/orbit_models.jpg" alt="Orbital Models" class="content-image">
    </div>
  </div>
</div>

### 2.2 Neural Network-Enhanced UDE

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Data-Driven Correction</div>
      <ul>
        <li>A neural network, implemented with Lux.jl, is embedded within the UDE to learn corrections to the orbital dynamics.</li>
        <li>SciML tools (OrdinaryDiffEq, ModelingToolkit, etc.) are employed to numerically solve the differential equations and obtain orbital trajectories.</li>
        <li>Gravitational waveforms are computed from the orbital paths using quadrupole formulas.</li>
      </ul>
    </div>
    <div>
      <img src="/images/neural_network_correction.jpg" alt="Neural Network Correction" class="content-image">
    </div>
  </div>
</div>

### 2.3 Training and Optimization

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Optimization Process</div>
      <ul>
        <li>A loss function quantifies the difference between the gravitational waveform predicted by the neural model and the reference waveform from the relativistic model.</li>
        <li>Training is performed using a hybrid strategy: initial optimization with ADAM followed by fine-tuning via BFGS.</li>
        <li>Callbacks visualize loss convergence and waveform evolution during training.</li>
      </ul>
    </div>
    <div>
      <img src="/images/optimization_process.jpg" alt="Optimization Process" class="content-image">
    </div>
  </div>
</div>

## 3. Results and Discussion

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Key Outcomes</div>
      <ul>
        <li><strong>Enhanced Waveform Prediction:</strong> The neural network-enhanced model accurately reproduces gravitational waveforms with relativistic corrections, outperforming the classical Newtonian prediction.</li>
        <li><strong>Orbit Trajectory Alignment:</strong> Predicted orbital paths closely match those obtained from the relativistic model, validating our data-driven approach.</li>
        <li><strong>Forecasting Capability:</strong> Extended simulations demonstrate the model's ability to predict long-term dynamics and waveform evolution.</li>
      </ul>
    </div>
    <div>
      <img src="/images/results_waveform.jpg" alt="Waveform Comparison" class="content-image">
    </div>
  </div>
</div>

## 4. Conclusion and Future Work

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <p>
        This project demonstrates that integrating neural networks with differential equation models using SciML in Julia can effectively capture relativistic corrections in black hole dynamics. The resulting model not only enhances gravitational waveform predictions but also offers deeper insights into orbital mechanics under strong gravitational fields.
      </p>
      <p>
        Future work will extend this methodology to binary systems with non-zero mass ratios, incorporate spin effects, and explore more sophisticated neural architectures to capture additional relativistic phenomena.
      </p>
    </div>
    <div>
      <img src="/images/future_work.jpg" alt="Future Work" class="content-image">
    </div>
  </div>
</div>

---
title: "SciML-Powered Neural Network Assisted Epidemic Modeling"
excerpt: "Leveraging SciML in Julia to develop a UDE framework that integrates neural networks with the SIR model for diagnosing COVID-19 quarantine effects.<br/><img src='/images/epidemic_model_thumbnail.jpg'>"
collection: portfolio
---

<style>
  .subpart-container {
    margin-top: 20px;
  }
  .content-row {
    display: grid;
    grid-template-columns: 2fr; /* single column for stacked images */
    /*grid-template-columns: 2fr 1fr; /* Two columns: text and images */
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
        The COVID-19 pandemic highlighted the need for robust, interpretable models that capture the effects of interventions such as quarantine and lockdowns. Traditional SIR models often lack the flexibility to handle complex, time-varying measures. This project enhances the SIR model by integrating a neural network within a Universal Differential Equation (UDE) framework, capturing the dynamic influence of quarantine measures on the epidemic's spread using Italy as a case study. 
      <div class="content-title">The project aims to answer the following questions:</div>
      </p>
  <ul>
    <li>How different were COVID-19 policies implemented by different countries?</li>
    <li>How many infections would have been prevented if some regions hadn’t reopened early?</li>
    <li>Can the next wave of the pandemic be predicted?</li>
    <li>What is the optimal social-distancing/lockdown policy to impose?</li>
  </ul>
      <p>
We look  at this project from a quarantine lens, and wheter we can make sciwntific ML driven decision on lockdown, quarantine policies and social distancing.
      <div class="content-title">What is an SIR model?</div>
      </p>
    </div>
    <div>
      <img src="/images/epidemic_intro.jpg" alt="Epidemic Model Overview" class="content-image">
      <img src="/images/epidemic_intro1.jpg" alt="Epidemic Model Overview1" class="content-image">
    </div>
  </div>
</div>

## 2. Methodology

### 2.1 Model Development

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Core Model</div>
      <p>
        The project extends the classical SIR framework to a QSIR model by adding a quarantine compartment. A neural network (built with Lux.jl) is embedded as a subtractive term in the infected equation to model the time-dependent quarantine strength, \( Q(t) \), using the current state \([S, I, R]\) as input.
      </p>
      <p>
        The differential equations are defined as:
      </p>
      <p>
        \( \frac{dS}{dt} = -\beta \frac{S I}{N} \)<br/>
        \( \frac{dI}{dt} = \beta \frac{S I}{N} - \gamma I - Q(t)\frac{I}{N} \)<br/>
        \( \frac{dR}{dt} = \gamma I + \delta T \)<br/>
        \( \frac{dT}{dt} = Q(t)\frac{I}{N} - \delta T \)
      </p>
    </div>
    <div>
      <!-- <img src="/images/model_equations.jpg" alt="Model Equations" class="content-image"> -->
    </div>
  </div>
</div>

### 2.2 Data and Preprocessing

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Data Integration</div>
      <ul>
        <li>Utilized COVID-19 data for Italy from the John Hopkins repository.</li>
        <li>Processed infected counts (adjusted to exclude recovered and deceased), recovered, and dead counts.</li>
        <li>Cleaned and structured time-series data to set initial conditions and parameters.</li>
      </ul>
    </div>
    <div>
      <img src="/images/data_preprocessing.png" alt="Data Preprocessing" class="content-image">
    </div>
  </div>
</div>

### 2.3 Training and Optimization

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Optimization Strategy</div>
      <ul>
        <li>Implemented a log-based loss function comparing predicted (infected + quarantined) and recovered counts to observed data.</li>
        <li>Utilized ADAM for initial optimization and BFGS for fine-tuning the neural network parameters.</li>
        <li>Employed adjoint sensitivity analysis via DifferentialEquations.jl and DiffEqFlux for efficient gradient computation.</li>
      </ul>
    </div>
    <div>
      <!-- <img src="/images/optimization_flow.jpg" alt="Optimization Flow" class="content-image"> -->
    </div>
  </div>
</div>

### 2.4 Model Diagnostics and Interpretation

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Diagnostic Insights</div>
      <ul>
        <li>Recovered time-dependent quarantine strength \( Q(t) \) and identified inflection points corresponding to government lockdown dates.</li>
        <li>Validated model predictions by comparing the temporal evolution of infected and recovered cases with actual data.</li>
      </ul>
    </div>
    <div>
      <img src="/images/quarantine_strength_plot.png" alt="Quarantine Strength \( Q(t) \)" class="content-image">
    </div>
  </div>
</div>


### 2.5 Model Performance

After training on Italy data, we evaluated on the full time series and obtained:

<table style="width:50%; margin:1em auto;">
  <thead>
    <tr><th style="text-align:left">Metric</th><th style="text-align:right">Value</th></tr>
  </thead>
  <tbody>
    <tr><td>RMSE</td><td>3 223.78</td></tr>
    <tr><td>MAE</td><td>2 296.41</td></tr>
    <tr><td>MAPE</td><td>3.91 %</td></tr>
    <tr><td>R²</td><td>0.9919</td></tr>
  </tbody>
</table>
These numbers indicate a very close fit between our UDE‐augmented SIR predictions and the ground truth.

<figure>
  <video controls width="100%" loop playsinline>
    <source src="/images/training_overlay.mp4" type="video/mp4">
    Your browser doesn’t support embedded videos.
  </video>
  <figcaption><em>Figure: Animated overlay of ground truth vs. model predictions.</em></figcaption>
</figure>

## 3. Results and Discussion

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <div class="content-title">Key Outcomes</div>
      <ul>
        <li><strong>Predictive Accuracy:</strong> The model successfully captures epidemic dynamics, achieving an R² of ~ 0.99 for the fit with ground truth.</li>
        <li><strong>Diagnostic Power:</strong> \( Q(t) \) closely aligns with the timing of Italy's lockdown, confirming its utility as a diagnostic tool.</li>
        <li><strong>Generalizability:</strong> Extended methodology to assess quarantine impacts in over 75 countries, with results publicly hosted at [covid19ml.org](https://covid19ml.org).</li>
      </ul>
    </div>
    <div>
      <img src="/images/final_overlay.png" alt="Prediction vs. Data" class="content-image">
    </div>
  </div>
</div>

## 4. Conclusion

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <p>
        This project demonstrates that integrating neural networks with traditional differential equation models using SciML in Julia can yield expressive and interpretable epidemic models. By capturing real-time quarantine dynamics, the framework not only improves forecasting of COVID-19 trends but also provides actionable diagnostic insights into public health interventions.
      </p>
    </div>
    <div>
      <!-- <img src="/images/model_conclusion.jpg" alt="Model Conclusion" class="content-image"> -->
    </div>
  </div>
</div>

<!-- ## 5. Future Work

<div class="subpart-container">
  <div class="content-row">
    <div class="content-text">
      <ul>
        <li>Extend the model to incorporate additional compartments (e.g., asymptomatic or hospitalized).</li>
        <li>Experiment with alternative neural network architectures and recurrent models to better capture temporal dependencies.</li>
        <li>Integrate diverse data sources (e.g., mobility, testing rates) to refine quarantine impact estimation.</li>
      </ul>
    </div>
  </div>
</div> -->

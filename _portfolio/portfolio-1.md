---
title: "Data-Driven Methods for Temperature Prediction"
excerpt: "Using machine learning methods such as Linear Regression and Neural Networks to predict temperature in heat transfer applications.<br/><img src='/images/temperature_prediction_thumbnail.png'>"
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
  /* Four images in a 2x2 grid */
  .images-four {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    margin-top: 15px;
  }
  /* Three images side by side */
  .images-three {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 15px;
    margin-top: 15px;
  }
  /* Three images stacked vertically */
  .images-three-vertical {
    display: grid;
    grid-template-columns: 1fr;
    gap: 15px;
    margin-top: 15px;
  }
  /* Two images side by side */
  .images-two {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    margin-top: 15px;
  }
  /* Single image */
  .images-one {
    display: grid;
    grid-template-columns: 1fr;
    gap: 15px;
    margin-top: 15px;
  }
  /* Responsive adjustments */
  @media (max-width: 768px) {
    .images-four {
      grid-template-columns: 1fr;
    }
    .images-three {
      grid-template-columns: 1fr;
    }
    .images-two {
      grid-template-columns: 1fr;
    }
  }
  @media (min-width: 769px) and (max-width: 1024px) {
    .images-three {
      grid-template-columns: 1fr 1fr;
    }
    .images-four {
      grid-template-columns: 1fr 1fr;
    }
  }
</style>


This project aims to utilize data-driven methods, including Linear Regression and Neural Networks, for predicting temperature coefficients based on simulated data. Below, we present the key subparts of the project, detailing each method and its implementation.

## Subpart 1: Linear Regression Heat Transfer Application

### Overview:
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section for What and How -->
    <div class="content-text">
      <div class="content-title">What?</div>
      <p>Build a model based on Linear Regression and Neural Networks to predict the heat transfer coefficient using data simulated with OpenFOAM. The model involves openfoam simulations for different physical features (u, rho, lambda, Cp).</p>

      <!-- 2 images side by side after "What?" -->
      <div class="images-two">
        <img src="/images/linear_regression_1.png" alt="Linear Regression Overview 1" class="content-image">
        <img src="/images/linear_regression_2.png" alt="Linear Regression Overview 2" class="content-image">
      </div>

      <div class="content-title">How?</div>
      <ul>
        <li>Dimensionless parameters (Re, Pr, Nu) were used to reduce the study to find Nu number.</li>
        <li>Data was uploaded on Google Colab for analysis.</li>
        <li>Calculated Re, Pr, Nu analytically using CFD data and plotted correlations.</li>
        <li>Plotted Nu correlation parity plots to evaluate data accuracy.</li>
        <li>Developed and compared analytical, linear regression, and neural network models to assess the accuracy and parity of Nu number predictions.</li>
      </ul>

      <!-- 2 images side by side after "How?" -->
      <div class="images-two">
        <img src="/images/how_method_1.png" alt="How Method 1" class="content-image">
        <img src="/images/how_method_2.png" alt="How Method 2" class="content-image">
      </div>
    </div>
  </div>
</div>


<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section -->
    <div class="content-text">
      <div class="content-title">Analytical Model</div>
      <ul>
        <li>Pre-processed and cleaned CFD results.</li>
        <li>Calculated Re, Pr, Nu from CFD data and plotted Re, Pr, Nu as functions of each other.</li>
      </ul>

      <!-- 4 images in 2x2 grid after "Analytical Model" -->
      <div class="images-four">
        <img src="/images/analytical_model1.png" alt="Analytical Model 1" class="content-image">
        <img src="/images/analytical_model2.png" alt="Analytical Model 2" class="content-image">
        <img src="/images/analytical_model3.png" alt="Analytical Model 3" class="content-image">
        <img src="/images/analytical_model4.png" alt="Analytical Model 4" class="content-image">
      </div>
    </div>
  </div>
</div>


<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section -->
    <div class="content-text">
      <div class="content-title">Naive Linear Regression</div>
      <ul>
        <li>Data was split into training and testing sets.</li>
        <li>Trained using the training data.</li>
        <li>Parity plots showed poor r² performance and high error.</li>
      </ul>

      <!-- 1 image after "Naive Linear Regression" -->
      <div class="images-one">
        <img src="/images/naive_linear_regression_1.png" alt="Naive Linear Regression 1" class="content-image">
      </div>
    </div>
  </div>
</div>

 
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section -->
    <div class="content-text">
      <div class="content-title">Elaborate Model (Ranz & Marshall)</div>
      <ul>
        <li>Used empirical coefficients C<sub>n,m</sub> to approximate Nu values.</li>
        <li>The elaborate model showed acceptable Nu correlation parity (in pink).</li>
      </ul>

      <!-- 3 images side by side after "Elaborate Model" -->
      <div class="images-three">
        <img src="/images/elaborate_model_1.png" alt="Elaborate Model 1" class="content-image">
        <img src="/images/elaborate_model_2.png" alt="Elaborate Model 2" class="content-image">
        <img src="/images/elaborate_model_3.png" alt="Elaborate Model 3" class="content-image">
      </div>
    </div>
  </div>
</div>

 
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section -->
    <div class="content-text">
      <div class="content-title">Neural Network</div>
      <ul>
        <li>Used dense neural network of 3 hidden layers; each layer = 64 neurons.</li>
        <li>Activation function: ReLU; Optimizer: Adam with a learning rate of 0.01.</li>
        <li>Mean absolute error used for metrics, and the neural network outperformed all models.</li>
      </ul>

      <!-- 2 images side by side after "Neural Network" -->
      <div class="images-two">
        <img src="/images/neural_network_1.png" alt="Neural Network 1" class="content-image">
        <img src="/images/neural_network_2.png" alt="Neural Network 2" class="content-image">
      </div>
    </div>
  </div>
</div>

## DNN Applied to Transient Heat Diffusion 1D

### Overview:
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section for What and How -->
    <div class="content-text">
      <div class="content-title">What?</div>
      <p>Build a Deep Neural Network to predict temperature evolution in a rod in a 1D transient thermal diffusion case. The rod material has a diffusion coefficient of a = 0.01 m²/s. Initial conditions: center of rod temperature = 400K, rest = 300K.</p>

      <!-- 3 images stacked vertically after "What?" -->
      <div class="images-three-vertical">
        <img src="/images/dnn_heat_diff_1d_1.png" alt="DNN Heat Diffusion 1D Overview 1" class="content-image">
        <img src="/images/dnn_heat_diff_1d_2.png" alt="DNN Heat Diffusion 1D Overview 2" class="content-image">
        <img src="/images/dnn_heat_diff_1d_3.png" alt="DNN Heat Diffusion 1D Overview 3" class="content-image">
      </div>

      <div class="content-title">How?</div>
      <ul>
        <li>Defined parameters like length, thermal diffusivity, total simulation time, time steps, and grid points.</li>
        <li>Defined initial temperature distribution and the diffusion equation matrix using the finite difference method.</li>
        <li>Developed a Deep Learning model with 2 hidden layers, each containing 128 units with ReLU activation.</li>
        <li>Tuned the model for well-agreeable accuracy with the calculated temperature distribution.</li>
      </ul>

      <!-- 2 images side by side after "How?" -->
      <div class="images-two">
        <img src="/images/dnn_1d_how_1.png" alt="DNN 1D How 1" class="content-image">
        <img src="/images/dnn_1d_how_2.png" alt="DNN 1D How 2" class="content-image">
      </div>
    </div>
  </div>
</div>

## DNN Applied to Transient Heat Diffusion 2D

### Overview:
<div class="subpart-container">
  <div class="content-row">
    <!-- Text Section for What and How -->
    <div class="content-text">
      <div class="content-title">What?</div>
      <p>Build a Deep Neural Network to predict temperature evolution over a square in a 2D transient thermal diffusion case. The surface material has a diffusion coefficient a = 0.01 m²/s. Initial conditions: center temperature = 400K, rest = 300K.</p>
      
      <!-- 3 images stacked vertically after "What?" -->
      <div class="images-three-vertical">
        <img src="/images/dnn_heat_diffusion_2d_1.png" alt="DNN Heat Diffusion 2D Overview 1" class="content-image">
        <img src="/images/dnn_heat_diffusion_2d_2.png" alt="DNN Heat Diffusion 2D Overview 2" class="content-image">
        <img src="/images/dnn_heat_diffusion_2d_3.png" alt="DNN Heat Diffusion 2D Overview 3" class="content-image">
      </div>
      
      <div class="content-title">How?</div>
      <ul>
        <li>Defined parameters such as the size of the square domain, thermal diffusivity, total simulation time, time steps, and grid points.</li>
        <li>Defined initial temperature distribution and set up the matrix for solving the diffusion equation using the finite difference method.</li>
        <li>Developed a Deep Learning model with 2 hidden layers of 128 units each and used ReLU as the activation function.</li>
        <li>Tuned the model to achieve accurate agreement with the calculated temperature distribution.</li>
      </ul>

      <!-- 3 images side by side after "How?" -->
      <div class="images-three">
        <img src="/images/dnn_2d_how_1.png" alt="DNN Heat Diffusion 2D Overview 1" class="content-image">
        <img src="/images/dnn_2d_how_2.png" alt="DNN Heat Diffusion 2D Overview 2" class="content-image">
        <img src="/images/dnn_2d_how_3.png" alt="DNN 2D How 3" class="content-image">
      </div>
    </div>
  </div>
</div>

<script setup>
import './sustainability.css'

import carImage from '../../assets/images/Car.jpg'
</script>

<template>
  <section class="vision-section">


    <div class="vision-label">
      <span class="vision-label-line"></span>

      Our Vision

      <span class="vision-label-line"></span>
    </div>

    <h2 class="vision-title">
      Built for Measure Sustainability
    </h2>

   
    <div class="vision-card">

     
      <div class="vision-image-wrap">
        <img
          :src="carImage"
          alt="GO-GENIE delivery truck"
          class="vision-img"
        />
      </div>

      
      <div class="vision-body">
        <p>
          At GO-GENIE®, sustainability starts with understanding your impact.
          We provide accurate, transparent carbon data and actionable insights
          so businesses can measure emissions, benchmark performance, and make
          informed decisions. Turning data into measurable, real-world impact.
        </p>
      </div>

    </div>
  </section>
</template>
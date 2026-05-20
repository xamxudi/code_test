<script setup>
import './reporting-section.css'

import cont1 from '../../assets/images/cont1.jpg'
import cont2 from '../../assets/images/cont2.jpg'
import cont3 from '../../assets/images/cont3.jpg'

const features = [
  {
    img: cont1,
    alt: 'Track Progress illustration',
    title: 'Track Progress',
    desc: 'Monitor your progress towards sustainability and certification targets.',
  },
  {
    img: cont2,
    alt: 'Generate Reports illustration',
    title: 'Generate Reports',
    desc: 'Create detailed reports for audits, compliance, and internal tracking.',
  },
  {
    img: cont3,
    alt: 'Showcase Achievements illustration',
    title: 'Showcase Achievements',
    desc: 'Highlight your sustainability efforts and build trust with customers.',
  },
]
</script>

<template>
  <section class="reporting-section">

    <div class="reporting-header">

      <h2>
        Simplify Sustainability
        <span class="highlight">
          Reporting and Compliance
        </span>
      </h2>

      <p>
        Track progress, generate reports
        and meet sustainability standards with ease.
      </p>

    </div>

    <div class="rows-wrap">

      <div
        v-for="item in features"
        :key="item.title"
        class="feature-row"
      >

        
        <div class="row-text">
          <h3>{{ item.title }}</h3>
          <p>{{ item.desc }}</p>
        </div>

       
        <div class="row-image">
          <img :src="item.img" :alt="item.alt" />
        </div>

      </div>

    </div>
  </section>
</template>
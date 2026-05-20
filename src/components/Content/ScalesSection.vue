<script setup>
import './scales-section.css'

import img4 from '../../assets/images/cont4.jpg'
import img5 from '../../assets/images/cont5.jpg'
import img6 from '../../assets/images/cont6.jpg'

const features = [
  {
    img: img4,
    alt: 'Data-Driven Insights',
    title: 'Data-Driven Insights',
    desc: 'Make informed decisions with accurate carbon tracking data.',
  },
  {
    img: img5,
    alt: 'Scalable Solutions',
    title: 'Scalable Solutions',
    desc: 'Apply sustainability practices across your entire logistics network.',
  },
  {
    img: img6,
    alt: 'Real Impact',
    title: 'Real Impact',
    desc: 'Reduce emissions while maintaining operational efficiency.',
  },
]
</script>

<template>
  <section class="scales-section">

    <div class="scales-header">

      <h2>
        Sustainability That
        <span class="highlight">
          Scales with Your Business
        </span>
      </h2>

      <p>
        Reduce emissions, improve efficiency,
        and operate more responsibly with GO-GENIE®.
      </p>

    </div>

    <div class="scales-grid">

      <div
        v-for="item in features"
        :key="item.title"
        class="scales-card"
      >

       
        <div class="card-img-wrap">
          <img :src="item.img" :alt="item.alt" />
        </div>

        
        <h3>{{ item.title }}</h3>
        <p>{{ item.desc }}</p>

      </div>

    </div>
  </section>
</template>
<script setup>
import './tracking-section.css'

const features = [
  {
    icon: 'lightning',
    color: 'blue',
    title: 'Optimise Delivery Routes',
    desc: 'Reduce emissions by optimising routes and improving delivery efficiency.',
  },
  {
    icon: 'eye',
    color: 'teal',
    title: 'Monitor Environmental Impact',
    desc: 'Track carbon emissions across shipments with real-time insights.',
  },
  {
    icon: 'home',
    color: 'amber',
    title: 'Achieve Sustainability Goals',
    desc: 'Set targets and measure progress toward your sustainability objectives.',
  },
]
</script>

<template>
  <section class="tracking-section">

    <div class="tracking-header">

      <h2>
        Real-Time Carbon Tracking
        <span class="highlight">
          for Every Delivery
        </span>
      </h2>

      <p>
        Monitor emissions, optimise routes,
        and improve sustainability across your logistics operations.
      </p>

    </div>

    <div class="cards-grid">

      <div
        v-for="item in features"
        :key="item.title"
        class="feature-card"
      >

        <div class="icon-wrap" :class="item.color">

          <svg
            v-if="item.icon === 'lightning'"
            viewBox="0 0 24 24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z"/>
          </svg>


          <svg
            v-if="item.icon === 'eye'"
            viewBox="0 0 24 24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <circle cx="12" cy="12" r="3"/>
            <path d="M2 12s3.6-7 10-7 10 7 10 7-3.6 7-10 7-10-7-10-7z"/>
          </svg>


          <svg
            v-if="item.icon === 'home'"
            viewBox="0 0 24 24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/>
            <path d="M9 22V12h6v10"/>
          </svg>

        </div>

        
        <div class="card-title">
          {{ item.title }}
        </div>

        <div class="card-desc">
          {{ item.desc }}
        </div>

      </div>

    </div>

  <button class="demo-btn">

      Book A Demo

      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path d="M9 18l6-6-6-6"/>
      </svg>

    </button>

  </section>
</template>
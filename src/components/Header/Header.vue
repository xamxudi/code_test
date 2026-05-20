<script setup>
import './header.css'
import headerImage from '../../assets/images/header-image.jpg'

const navItems = [
  {
    label: 'Services',
    dropdown: ['Express Delivery', 'Same Day', 'International', 'Bulk Shipping']
  },
  {
    label: 'Solutions',
    dropdown: ['For Business', 'For E-commerce', 'For Enterprise']
  },
  {
    label: 'About',
    dropdown: ['Our Story', 'Careers', 'Press', 'Contact']
  },
  {
    label: 'Help & Guides',
    dropdown: ['FAQ', 'Shipping Guide', 'Support']
  }
]
</script>

<template>
  <nav class="navbar">
    <div class="navbar-inner">

      <div class="logo">GO-GENIE</div>

      <ul class="nav-links">
        <li
          v-for="item in navItems"
          :key="item.label"
          class="nav-item"
        >
          <a href="#" class="nav-link" @click.prevent>
            {{ item.label }}

            <svg class="chevron" viewBox="0 0 12 8" fill="none">
              <path
                d="M1 1l5 5 5-5"
                stroke="currentColor"
                stroke-width="1.8"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </a>

          <div class="dropdown">
            <a
              v-for="sub in item.dropdown"
              :key="sub"
              href="#"
              class="dropdown-item"
            >
              {{ sub }}
            </a>
          </div>
        </li>
      </ul>


      <div class="nav-actions">
        <button class="btn-track">
          Track Your Parcel
        </button>

        <button class="btn-signin">
          Sign In
        </button>

        <div class="lang-selector">
          <img
            src="https://flagcdn.com/w40/gb.png"
            alt="English"
            class="flag"
          />

          <svg class="chevron" viewBox="0 0 12 8" fill="none">
            <path
              d="M1 1l5 5 5-5"
              stroke="currentColor"
              stroke-width="1.8"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
      </div>
    </div>
  </nav>

  <section class="hero-section">

    
    <div class="hero-text">
      <h1>
        Measure and Reduce Your Logistics Carbon Footprint
      </h1>

      <p>
        Track emissions, gain real-time insights,
        and make smarter, more sustainable logistics decisions.
      </p>

      <button class="hero-btn">
        Explore Sustainability Solutions

        <svg viewBox="0 0 24 24" fill="none" class="hero-btn-arrow">
          <path
            d="M9 18l6-6-6-6"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </button>
    </div>

   
    <div class="hero-city">
      <img
        :src="headerImage"
        alt="Logistics city illustration"
        class="hero-img"
      />
    </div>

  </section>
</template>
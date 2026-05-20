<script setup>
import './footer.css'

import logo8  from '../../assets/images/f8.jpg'
import logo9  from '../../assets/images/f9.jpg'
import logo10 from '../../assets/images/f10.jpg'
import logo11 from '../../assets/images/f11.jpg'

const navColumns = [
  {
    heading: 'Services',
    links: ['Last-Mile Delivery', 'Warehousing', 'Fulfilment'],
  },
  {
    heading: 'Solutions',
    links: ['Merchants', 'Service Providers', 'Gig Workers'],
  },
  {
    heading: 'About',
    links: ['GO-GENIE®', 'Our Ecosystem', 'Sustainability', 'Newsroom'],
  },
  {
    heading: 'Help & Guides',
    links: ['Help Center', 'Contact Us'],
  },
  {
    heading: 'Quick Links',
    links: ['Privacy Policy', 'Terms of Service', 'Data Retention Policy'],
  },
]

const awards = [
  'Brands For Good 2025 - Honouree',
  'SPBA 2025 - Promising Brands',
  'SPBA 2025 - Transformation Efforts',
]

const chambers = [
  'Member of Singapore Chinese Chamber of Commerce & Industry (SCCCI)',
  'Member of Singapore Business Federation (SBF)',
]

const awardLogos = [
  { src: logo8, alt: 'Singapore Prestige Brand Award 2025' },
  { src: logo9, alt: 'Brands for Good' },
  { src: logo10, alt: 'Singapore Chinese Chamber' },
  { src: logo11, alt: 'Singapore Business Federation' },
]
</script>

<template>
  <footer class="footer">

    <div class="footer-top">

      <div class="footer-inner">

        <div class="footer-logo">
          GO-GENIE
        </div>

        <div class="footer-divider"></div>

        <div class="footer-nav">

          <div
            v-for="col in navColumns"
            :key="col.heading"
            class="footer-col"
          >

            <div class="col-heading">
              {{ col.heading }}
            </div>

            <a
              v-for="link in col.links"
              :key="link"
              href="#"
              class="col-link"
            >
              {{ link }}
            </a>

          </div>

        </div>

        <div class="footer-divider"></div>

        <div class="footer-bottom-row">

          <div class="address-block">
            <p>
              <strong>Singapore Address:</strong>
              1234 Building, Random Rd,
              Singapore, 17890123
            </p>
          </div>

          <div class="address-block">
            <p>
              <strong>Vietnam Address:</strong>
              1234 Rd, Random District,
              Ho Chi Minh City, Vietnam
            </p>
          </div>

          <div class="social-block">

            <p class="social-label">
              Follow us and keep updated
            </p>

            <div class="social-icons">

              <a href="#" class="social-icon" aria-label="Facebook">
                <svg viewBox="0 0 24 24" fill="currentColor">
                  <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"/>
                </svg>
              </a>

              <a href="#" class="social-icon" aria-label="Instagram">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <rect x="2" y="2" width="20" height="20" rx="5"/>
                  <circle cx="12" cy="12" r="4"/>
                  <circle cx="17.5" cy="6.5" r="0.5" fill="currentColor"/>
                </svg>
              </a>

              <a href="#" class="social-icon" aria-label="TikTok">
                <svg viewBox="0 0 24 24" fill="currentColor">
                  <path d="M19.59 6.69a4.83 4.83 0 01-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 01-2.88 2.5 2.89 2.89 0 01-2.89-2.89 2.89 2.89 0 012.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 00-.79-.05 6.34 6.34 0 00-6.34 6.34 6.34 6.34 0 006.34 6.34 6.34 6.34 0 006.33-6.34V8.69a8.18 8.18 0 004.78 1.52V6.76a4.85 4.85 0 01-1.01-.07z"/>
                </svg>
              </a>

              <a href="#" class="social-icon" aria-label="X">
                <svg viewBox="0 0 24 24" fill="currentColor">
                  <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
                </svg>
              </a>

            </div>
          </div>

        </div>
      </div>
    </div>

    <div class="footer-awards">

      <div class="footer-inner awards-inner">

        
        <div class="awards-text">

          <div class="awards-group">

            <p class="awards-heading">
              Awards and Recognition
            </p>

            <p
              v-for="a in awards"
              :key="a"
              class="awards-item"
            >
              {{ a }}
            </p>

          </div>

          <div class="awards-group">

            <p class="awards-heading">
              Business Chambers
            </p>

            <p
              v-for="c in chambers"
              :key="c"
              class="awards-item"
            >
              {{ c }}
            </p>

          </div>

        </div>

        <div class="award-logos">

          <img
            v-for="logo in awardLogos"
            :key="logo.alt"
            :src="logo.src"
            :alt="logo.alt"
            class="award-logo-img"
          />

        </div>

      </div>
    </div>

    <div class="footer-copy">
      <p>
        © 2026 GO-GENIE® All Rights Reserved.
      </p>
    </div>

  </footer>
</template>
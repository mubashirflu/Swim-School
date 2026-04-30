<template>
  <section class="imagine-section">
    <div class="container">

      <!-- Heading -->
      <h2 class="main-heading">
        Imagine Walking Into the<br> Water Calm and Confident
      </h2>

      <p class="sub-text">
        You’re on vacation. Your friends run toward the pool or ocean and this time, you don’t stay behind.<br>
        This isn’t just swim lessons — it’s self-trust, confidence, and freedom in the water.
      </p>

      <!-- Slider -->
      <div class="slider-wrapper">

        <div class="slider-container">
          <div 
            class="slider-track" 
            :style="{ transform: `translateX(-${currentIndex * slideWidth}%)` }"
          >
            <div 
              v-for="(slide, index) in slides" 
              :key="index" 
              class="slide"
              :class="{ active: index === currentIndex }"
            >
              <img :src="slide.img" :alt="slide.title" />
              <p class="slide-caption">{{ slide.title }}</p>
            </div>
          </div>
        </div>

        <!-- Controls -->
        <div class="controls-row">

          <div class="slider-controls">
            <button class="nav-btn" @click="prevSlide">←</button>
            <button class="nav-btn" @click="nextSlide">→</button>
          </div>

          <button class="journey-btn" @click="startJourney">
            Start Your Journey
          </button>

        </div>

      </div>

    </div>
  </section>
</template>

<script>
import img1 from '@/assets/Modern Architectural Structure at Dusk (6).png'
import img2 from '@/assets/Modern Architectural Structure at Dusk (7).png'
import img3 from '@/assets/Modern Architectural Structure at Dusk (8).png'
import img4 from '@/assets/Modern Architectural Structure at Dusk (9).png'

export default {
  name: 'ImagineSlider',
  data() {
    return {
      currentIndex: 0,
      isMobile: false,
      slides: [
        { img: img1, title: 'You Walk In Calmly.' },
        { img: img2, title: 'You Breathe Steadily.' },
        { img: img3, title: 'Your Body Moves Naturally.' },
        { img: img4, title: 'You Feel Strong. You Feel Free.' }
      ]
    }
  },

  computed: {
    slideWidth() {
      if (this.isMobile) return 100
      if (window.innerWidth <= 1024) return 50
      return 25
    }
  },

  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.slides.length
    },
    prevSlide() {
      this.currentIndex =
        (this.currentIndex - 1 + this.slides.length) % this.slides.length
    },
    startJourney() {
      alert('Starting your swimming journey!')
    },
    checkScreen() {
      this.isMobile = window.innerWidth <= 768
    }
  },

  mounted() {
    this.checkScreen()
    window.addEventListener('resize', this.checkScreen)
  },

  beforeUnmount() {
    window.removeEventListener('resize', this.checkScreen)
  }
}
</script>

<style scoped>

/* ================= BASE ================= */
.imagine-section {
  padding: 50px 20px;
  background: white;
  text-align: center;
}

.container {
  max-width: 1280px;
  margin: 0 auto;
}

/* ================= HEADING ================= */
.main-heading {
  font-size: 44px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 700;
  color: #1F4E5F;
  margin-bottom: 16px;
  line-height: 1.2;
}

.sub-text {
  font-size: 16px;
  font-family: 'DM Sans', sans-serif;
  color: #555;
  max-width: 650px;
  margin: 0 auto 50px;
  line-height: 1.6;
}

/* ================= SLIDER ================= */
.slider-wrapper {
  max-width: 1200px;
  margin: 0 auto;
}

.slider-container {
  overflow: hidden;
}

.slider-track {
  display: flex;
  transition: transform 0.7s ease;
}

.slide {
  min-width: 25%;
  padding: 0 10px;
  transition: 0.5s ease;
  opacity: 0.7;
  transform: scale(0.95);
}

.slide.active {
  opacity: 1;
  transform: scale(1);
}

.slide img {
  width: 100%;
  height: 280px;
  object-fit: cover;
  border-radius: 16px;
}

.slide-caption {
  margin-top: 12px;
  font-size: 16px;
  font-weight: 600;
  color: #333;
}

/* ================= CONTROLS ================= */
.controls-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
  gap: 20px;
  flex-wrap: wrap;
}

.slider-controls {
  display: flex;
  gap: 12px;
}

.nav-btn {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  border: 2px solid #333;
  background: white;
  cursor: pointer;
  font-size: 22px;
}

.nav-btn:hover {
  background: #333;
  color: white;
}

/* ✅ FIXED BUTTON */
.journey-btn {
  background: #1F4E5F;
  color: white;
  border: none;
  padding: 12px 18px;
  font-size: 15px;
  border-radius: 38px;
  cursor: pointer;
  white-space: nowrap;
  width: auto;
  display: inline-block;
  transition: 0.3s;
}

.journey-btn:hover {
  transform: translateY(-3px);
}

/* ================= RESPONSIVE ================= */

/* Tablet */
@media (max-width: 1024px) {
  .slide {
    min-width: 50%;
  }

  .main-heading {
    font-size: 36px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .slide {
    min-width: 100%;
  }

  .main-heading {
    font-size: 30px;
  }

  .controls-row {
    flex-direction: column;
  }
}

/* Small Mobile */
@media (max-width: 360px) {
  .imagine-section {
    padding: 30px 12px;
  }

  .main-heading {
    font-size: 24px;
  }

  .sub-text {
    font-size: 13px;
  }

  .slide img {
    height: 220px;
  }

  .journey-btn {
    font-size: 14px;
    padding: 10px 16px;
  }
}

</style>
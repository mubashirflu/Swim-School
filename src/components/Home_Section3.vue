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

        <!-- Arrows + Button Row -->
        <div class="controls-row">
          <!-- Left Side: Arrows -->
          <div class="slider-controls">
            <button class="nav-btn prev" @click="prevSlide">←</button>
            <button class="nav-btn next" @click="nextSlide">→</button>
          </div>

          <!-- Right Side: Start Your Journey Button -->
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
      return this.isMobile ? 100 : 25
    }
  },

  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.slides.length
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.slides.length) % this.slides.length
    },
    goToSlide(index) {
      this.currentIndex = index
    },
    startJourney() {
      alert('Starting your swimming journey!')
    },
    checkMobile() {
      this.isMobile = window.innerWidth < 769
    }
  },

  mounted() {
    this.checkMobile()
    window.addEventListener('resize', this.checkMobile)
  },

  beforeUnmount() {
    window.removeEventListener('resize', this.checkMobile)
  }
}
</script>

<style scoped>
.imagine-section {
  padding: 50px 20px 50px;
  background: white;
  text-align: center;
}

.container {
  max-width: 1280px;
  margin: 0 auto;
}

.main-heading {
  font-size: 44px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 700;
  color: #1F4E5F;
  margin-bottom: 16px;
  line-height: 1.15;
}

.sub-text {
  font-size: 16.5px;
  font-family: 'DM Sans', sans-serif;
  color: #555;
  max-width: 650px;
  margin: 0 auto 60px;
  text-align: center;
  line-height: 1.6;
}

/* ============= Slider ============= */
.slider-wrapper {
  max-width: 1200px;
  margin: 0 auto 40px;
  position: relative;
}

.slider-container {
  overflow: hidden;
}

.slider-track {
  display: flex;
  transition: transform 0.7s cubic-bezier(0.25, 0.1, 0.25, 1);
}

.slide {
  min-width: 25%;
  padding: 0 12px;
  box-sizing: border-box;
  transition: all 0.6s ease;
  opacity: 0.75;
  transform: scale(0.93) rotateY(10deg);
}

.slide.active {
  opacity: 1;
  transform: scale(1) rotateY(0deg);
}

.slide img {
  width: 100%;
  height: 280px;
  object-fit: cover;
  border-radius: 18px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
  transition: transform 0.5s ease;
}

.slide:hover img {
  transform: scale(1.05);
}

.slide-caption {
  margin-top: 16px;
  font-size: 16.5px;
  font-family: 'DM Sans', sans-serif;
  color: #333333;
  font-weight: 600;
  text-align: center;
}

/* ================== Controls Row (Arrows + Button) ================== */
.controls-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 20px;
  flex-wrap: wrap;
  gap: 20px;
}

.slider-controls {
  display: flex;
  gap: 16px;
  justify-content: flex-start;
}

.nav-btn {
  width: 45px;
  height: 45px;
  background: white;
  color: #333333;
  border: 2px solid #333333;
  font-size: 28px;
  border-radius: 50%;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.nav-btn:hover {
  background: #333333;
  color: white;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.2);
}

.nav-btn:active {
  transform: scale(0.95);
}

/* Journey Button */
.journey-btn {
  background: #1F4E5F;
  color: white;
  border: none;
  padding: 16px 24px 16px 24px;
  font-size: 16.5px;
  font-family: 'DM Sans', sans-serif;
  font-weight:500px;
  border-radius: 38px;
  cursor: pointer;
  transition: all 0.4s ease;
  box-shadow: 0 6px 20px rgba(30, 64, 175, 0.25);
  white-space: nowrap;
}

.journey-btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 25px rgba(30, 64, 175, 0.35);
}
/* Responsive */
@media (max-width: 768px) {
  .slider-wrapper {
    max-width: 100%;
  }

  .controls-row {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .slider-controls {
    margin: 0;
  }

  .slide {
    min-width: 100%;
    padding: 0 8px;
    transform: scale(0.96);
  }

  .slide img {
    height: 250px;
  }

  .main-heading {
    font-size: 36px;
  }

  .nav-btn {
    width: 42px;
    height: 42px;
    font-size: 24px;
  }

  .journey-btn {
    padding: 14px 32px;
    font-size: 1.05rem;
  }
}
</style>
<template>
  <section class="imagine-section">
    <div class="container">
      <!-- Heading -->
      <h2 class="main-heading">
        Imagine Walking Into the Water Calm and Confident
      </h2>
      <p class="sub-text">
        You don’t just learn to swim. You build trust, confidence, and freedom in the water.
      </p>

      <!-- Slider -->
      <div class="slider-wrapper">
        <button class="nav-btn prev" @click="prevSlide">‹</button>

        <div class="slider-container">
          <div 
            class="slider-track" 
            :style="{ transform: `translateX(-${currentIndex * 25}%)` }"
          >
            <div v-for="(slide, index) in slides" :key="index" class="slide">
              <img :src="slide.img" :alt="slide.title" />
              <p class="slide-caption">{{ slide.title }}</p>
            </div>
          </div>
        </div>

        <button class="nav-btn next" @click="nextSlide">›</button>
      </div>

      <!-- Dots -->
      <div class="dots">
        <span 
          v-for="(slide, index) in slides" 
          :key="index"
          class="dot"
          :class="{ active: index === currentIndex }"
          @click="goToSlide(index)"
        ></span>
      </div>

      <!-- Bottom Text and Button -->
      <div class="bottom-row">
        <div class="breathe-text">
          You Breathe Steadily.
        </div>
        <button class="journey-btn" @click="startJourney">
          Start Your Journey
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ImagineSlider',
  data() {
    return {
      currentIndex: 0,
      slides: [
        {
          img: '@/assets/Modern Architectural Structure at Dusk (6).png',
          title: 'You Walk In Calmly.'
        },
        {
          img: '@/assets/Modern Architectural Structure at Dusk (7).png',
          title: 'You Breathe Steadily.'
        },
        {
          img: '@/assets/Modern Architectural Structure at Dusk (8).png',
          title: 'Your Body Moves Naturally.'
        },
        {
          img: '@/assets/Modern Architectural Structure at Dusk (9).png',
          title: 'You Feel Strong. You Feel Free.'
        }
      ]
    }
  },
  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.slides.length;
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.slides.length) % this.slides.length;
    },
    goToSlide(index) {
      this.currentIndex = index;
    },
    startJourney() {
      alert('Starting your swimming journey!'); // Yahan apna routing ya modal daal sakte ho
    }
  }
}
</script>

<style scoped>
.imagine-section {
  padding: 80px 20px 100px;
  background: white;
  text-align: center;
}

.container {
  max-width: 1280px;
  margin: 0 auto;
}

.main-heading {
  font-size: 2.75rem;
  font-weight: 700;
  color: #1e40af;
  margin-bottom: 12px;
}

.sub-text {
  font-size: 1.15rem;
  color: #475569;
  max-width: 700px;
  margin: 0 auto 50px;
}

/* ============= Slider ============= */
.slider-wrapper {
  position: relative;
  max-width: 1000px;
  margin: 0 auto 40px;
}

.slider-container {
  overflow: hidden;
  border-radius: 16px;
}

.slider-track {
  display: flex;
  transition: transform 0.5s ease;
}

.slide {
  min-width: 25%;
  padding: 0 10px;
  box-sizing: border-box;
}

.slide img {
  width: 100%;
  height: 260px;
  object-fit: cover;
  border-radius: 12px;
}

.slide-caption {
  margin-top: 12px;
  font-size: 1.1rem;
  color: #1e3a8a;
  font-weight: 500;
}

/* Navigation Buttons */
.nav-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(30, 64, 175, 0.85);
  color: white;
  border: none;
  width: 50px;
  height: 50px;
  font-size: 28px;
  border-radius: 50%;
  cursor: pointer;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: 0.3s;
}

.nav-btn:hover {
  background: #1e40af;
}

.prev { left: -25px; }
.next { right: -25px; }

/* Dots */
.dots {
  display: flex;
  justify-content: center;
  gap: 12px;
  margin-bottom: 50px;
}

.dot {
  width: 14px;
  height: 14px;
  background: #cbd5e1;
  border-radius: 50%;
  cursor: pointer;
  transition: 0.3s;
}

.dot.active {
  background: #1e40af;
  transform: scale(1.3);
}

/* Bottom Row */
.bottom-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 800px;
  margin: 0 auto;
  flex-wrap: wrap;
  gap: 20px;
}

.breathe-text {
  font-size: 1.35rem;
  font-weight: 600;
  color: #334155;
}

.journey-btn {
  background: #1e40af;
  color: white;
  border: none;
  padding: 14px 36px;
  font-size: 1.1rem;
  font-weight: 600;
  border-radius: 50px;
  cursor: pointer;
  transition: 0.3s;
}

.journey-btn:hover {
  background: #1e3a8a;
  transform: translateY(-2px);
}

/* Responsive */
@media (max-width: 992px) {
  .nav-btn {
    width: 44px;
    height: 44px;
    font-size: 24px;
  }
  .prev { left: -15px; }
  .next { right: -15px; }
}

@media (max-width: 768px) {
  .slide { min-width: 100%; }
  .slider-track { transform: none !important; } /* Optional: disable translate on mobile if needed */
}
</style>
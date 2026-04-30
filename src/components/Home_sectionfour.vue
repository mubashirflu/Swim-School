<template>
  <section class="meet-section">
    <div class="container">

      <div class="meet-content">

        <!-- LEFT -->
        <div class="text-content">

          <h2 class="main-heading">Meet Rachael</h2>

          <p class="description">
            Rachael Locke is a swim instructor and coach dedicated to helping both 
            adults and children feel safe, supported, and confident in the water.
          </p>

          <p class="description">
            She specializes in working with adults who carry fear, anxiety, or past 
            negative experiences around swimming. Her approach is patient, trauma-
            aware, and completely personalized because no two swimmers are the same.
          </p>

          <p class="description">
            Rachael believes learning to swim isn’t just about technique. 
            It’s about building trust in your body and confidence in yourself.
          </p>

          <button class="clarity-btn" @click="bookCall">
            Book Your Free Clarity Call
          </button>

          <!-- bottom boxes -->
          <div class="bottom-info">

            <div class="info-box">
              <h3>Book A Free Clarity Call</h3>
              <p>We talk about your goals, fears, and experience.</p>
            </div>

            <div class="info-box">
              <h3>Build Confidence & Skill</h3>
              <p>We move gently at your pace.<br>Breath by breath. Stroke by stroke.</p>
            </div>

          </div>

        </div>

        <!-- RIGHT IMAGE -->
        <div class="image-container">
          <img 
            src="@/assets/Modern Architectural Structure at Dusk (10).png" 
            alt="Rachael swimming"
            class="rachael-image"
          />
        </div>

      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: 'MeetRachael',
  methods: {
    bookCall() {
      alert('Opening Free Clarity Call booking...')
    }
  }
}
</script>

<style scoped>

/* ================= BASE ================= */
.meet-section {
  padding: 60px 20px;
  background: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

/* ================= LAYOUT ================= */
.meet-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

/* ================= TEXT ================= */
.text-content {
  width: 100%;
}

.main-heading {
  font-size: 44px;
  font-weight: 600;
  color: #1F4E5F;
  margin-bottom: 20px;
  line-height: 1.2;
  font-family: 'DM Sans', sans-serif;
}

.description {
  font-size: 16px;
  line-height: 1.75;
  color: #444;
  margin-bottom: 18px;
  font-family: 'DM Sans', sans-serif;
}

/* ================= BUTTON ================= */
.clarity-btn {
  background: #1F4E5F;
  color: white;
  border: none;
  padding: 14px 22px;
  font-size: 15px;
  font-weight: 600;
  border-radius: 38px;
  cursor: pointer;
  margin: 20px 0 35px;
  transition: 0.3s;
  display: inline-block;
}

.clarity-btn:hover {
  transform: translateY(-3px);
}

/* ================= BOTTOM BOXES ================= */
.bottom-info {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
}

.info-box h3 {
  font-size: 18px;
  font-weight: 600;
  color: #333;
  margin-bottom: 6px;
}

.info-box p {
  font-size: 14px;
  color: #555;
  line-height: 1.6;
}

/* ================= IMAGE ================= */
.image-container {
  width: 100%;
}

.rachael-image {
  width: 100%;
  height: 550px;
  object-fit: cover;
  border-radius: 16px;
}

/* ================= RESPONSIVE ================= */

/* Tablet */
@media (max-width: 1024px) {
  .meet-content {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .main-heading {
    font-size: 36px;
  }

  .rachael-image {
    height: 450px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .main-heading {
    font-size: 30px;
  }

  .description {
    font-size: 14px;
  }

  .bottom-info {
    grid-template-columns: 1fr;
  }

  .clarity-btn {
    width: auto;
  }

  .rachael-image {
    height: 380px;
  }
}

/* Small Mobile 320px safe */
@media (max-width: 360px) {
  .meet-section {
    padding: 40px 12px;
  }

  .main-heading {
    font-size: 24px;
  }

  .description {
    font-size: 13px;
  }

  .clarity-btn {
    width: 100%;
    text-align: center;
  }

  .rachael-image {
    height: 300px;
  }
}

</style>
<template>
  <section class="meet-section">
    <div class="container">
      <div class="meet-content">
        <!-- Left Text Content -->
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

          <!-- Bottom Two Columns -->
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

        <!-- Right Image -->
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
      alert('Opening Free Clarity Call booking...');
      // TODO: Add actual booking logic or modal here
    }
  }
}
</script>

<style scoped>
.meet-section {
  padding: 50px 20px;
  background: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.meet-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.text-content {
  max-width: 520px;
}

.main-heading {
  font-size: 44px;
  font-weight: 600;
  color: #1F4E5F;
  margin-bottom: 24px;
  line-height: 1.2;
  font-family: 'DM Sans', sans-serif;
}

.description {
  font-size: 16px;
  line-height: 1.75;
  color: #444444;
  margin-bottom: 20px;
  font-family: 'DM Sans', sans-serif;
}

.clarity-btn {
  background: #1F4E5F;
  color: white;
  border: none;
  padding: 16px 24px 16px 24px;
  font-size: 16px;
  font-weight: 600;
  border-radius: 38px;
  cursor: pointer;
  margin: 20px 0 40px;
  transition: all 0.3s ease;
  font-family: 'DM Sans', sans-serif;
}

.clarity-btn:hover {
  background: #1F4E5F;
  transform: translateY(-2px);
}

.bottom-info {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
}

.info-box h3 {
  font-size: 20px;
  font-weight: 600;
  color: #333333;
  margin-bottom: 8px;
  font-family: 'DM Sans', sans-serif;
}

.info-box p {
  font-size: 15px;
  line-height: 1.6;
  color: #555;
  font-family: 'DM Sans', sans-serif;
}

/* Image */
.image-container {
  position: relative;
}

.rachael-image {
  width: 100%;
  height: 600px;
  border-radius: 16px;
  /* box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12); */
  object-fit: cover;
}

/* Responsive */
@media (max-width: 992px) {
  .meet-content {
    grid-template-columns: 1fr;
    gap: 50px;
  }
  
  .main-heading {
    font-size: 36px;
  }
  
  .bottom-info {
    gap: 30px;
  }
}

@media (max-width: 576px) {
  .bottom-info {
    grid-template-columns: 1fr;
    gap: 25px;
  }
}
</style>
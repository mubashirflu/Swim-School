<template>
  <div>
    <section class="upper-section">
      <div class="container">

        <!-- HEADER -->
        <div class="header">
          <h2>A Different Kind of Swim Experience</h2>
          <p class="subtitle">
            At Growing Space LLC, we offer a personalized, patient, coaching-focused, and supportive approach to swimming.
          </p>
        </div>

        <!-- CARDS -->
        <div class="cards-grid">

          <div class="card">
            <img src="@/assets/Modern Architectural Structure at Dusk (3).png" />
            <div class="card-content">
              <h3>Adult Private Swim Coaching</h3>
              <p>Overcome your fear and learn to swim at your own pace in a supportive environment.</p>
              <button class="card-btn">Book Adult Sessions</button>
            </div>
          </div>

          <div class="card">
            <img src="@/assets/Modern Architectural Structure at Dusk (4).png" />
            <div class="card-content">
              <h3>Kids Swim Sessions</h3>
              <p>Fun, safe, and effective swimming lessons for children of all ages and skill levels.</p>
              <button class="card-btn">Book Kids Sessions</button>
            </div>
          </div>

          <div class="card">
            <img src="@/assets/Modern Architectural Structure at Dusk (5).png" />
            <div class="card-content">
              <h3>Intensive Adult Clinics</h3>
              <p>Accelerated programs for faster progress and confidence building.</p>
              <button class="card-btn">Explore Clinics</button>
            </div>
          </div>

        </div>

      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'SwimExperienceSection'
}
</script>

<style scoped>

/* ================= BASE ================= */
.upper-section {
  background: #F0F7FF;
  padding: 60px 20px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

/* ================= HEADER ================= */
.header {
  text-align: center;
  margin-bottom: 50px;
}

.header h2 {
  font-size: 44px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 700;
  color: #1F4E5F;
  margin-bottom: 16px;
  line-height: 1.2;
}

.subtitle {
  font-size: 20px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 400;
  color: #1F4E5F;
  max-width: 750px;
  margin: 0 auto;
  line-height: 1.6;
}

/* ================= GRID ================= */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}

/* ================= CARD ================= */
.card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.08);
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-8px);
}

.card img {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.card-content {
  padding: 24px;
  text-align: center;
}

.card-content h3 {
  font-size: 22px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color: #333;
  margin-bottom: 12px;
}

.card-content p {
  font-size: 16px;
  font-family: 'DM Sans', sans-serif;
  color: #333;
  margin-bottom: 18px;
  line-height: 1.6;
}

/* ================= BUTTON ================= */
.card-btn {
  font-size: 15px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color: white;
  background-color: #1F4E5F;
  border: none;
  padding: 14px 22px;
  border-radius: 38px;
  cursor: pointer;
  transition: 0.3s;
}

.card-btn:hover {
  background-color: #163d4a;
  transform: translateY(-2px);
}

/* ================= RESPONSIVE ================= */

/* Tablet */
@media (max-width: 1024px) {
  .cards-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .header h2 {
    font-size: 36px;
  }

  .subtitle {
    font-size: 18px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .cards-grid {
    grid-template-columns: 1fr;
  }

  .header h2 {
    font-size: 30px;
  }

  .subtitle {
    font-size: 16px;
  }

  .card-content h3 {
    font-size: 20px;
  }

  .card-content p {
    font-size: 14px;
  }
}

/* Small Mobile (320px safe) */
@media (max-width: 360px) {
  .upper-section {
    padding: 40px 12px;
  }

  .header h2 {
    font-size: 24px;
  }

  .subtitle {
    font-size: 14px;
  }

  .card-content {
    padding: 18px;
  }

  .card-btn {
    width: 100%;
    font-size: 14px;
    padding: 12px;
  }
}
@media (max-width: 1200px) {
  .cards-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Tablet (safe 2 cards) */
@media (max-width: 1024px) {
  .cards-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .header h2 {
    font-size: 36px;
  }

  .subtitle {
    font-size: 18px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .cards-grid {
    grid-template-columns: 1fr;
  }

  .header h2 {
    font-size: 30px;
  }

  .subtitle {
    font-size: 16px;
  }

  .card-content h3 {
    font-size: 20px;
  }

  .card-content p {
    font-size: 14px;
  }
}

/* Small Mobile (320px safe) */
@media (max-width: 360px) {
  .upper-section {
    padding: 40px 12px;
  }

  .header h2 {
    font-size: 24px;
  }

  .subtitle {
    font-size: 14px;
  }

  .card-content {
    padding: 18px;
  }

  .card-btn {
    width: 100%;
    font-size: 14px;
    padding: 12px;
  }
}
</style>
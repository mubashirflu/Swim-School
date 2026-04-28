<template>
  <div>
    <section class="upper-section">
      <div class="container">
        <div class="header">
          <h2>A Different Kind of Swim Experience</h2>
          <p class="subtitle">
            At Growing Space LLC, we offer a personalized, patient, coaching-focused, and supportive approach to swimming.
          </p>
        </div>

        <div class="cards-grid">
          <div class="card">
            <img src="@/assets/Modern Architectural Structure at Dusk (3).png" alt="Adult Private Swim Coaching" />
            <div class="card-content">
              <h3>Adult Private Swim Coaching</h3>
              <p>Overcome your fear and learn to swim at your own pace in a supportive environment.</p>
              <button class="card-btn">Book Adult Sessions</button>
            </div>
          </div>
          <div class="card">
            <img src="@/assets/Modern Architectural Structure at Dusk (4).png" alt="Kids Swim Sessions" />
            <div class="card-content">
              <h3>Kids Swim Sessions</h3>
              <p>Fun, safe, and effective swimming lessons for children of all ages and skill levels.</p>
              <button class="card-btn">Book Kids Sessions</button>
            </div>
          </div>
          <div class="card">
            <img src="@/assets/Modern Architectural Structure at Dusk (5).png" alt="Intensive Adult Clinics" />
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
.upper-section {
  background: #f0f7ff;
  padding: 60px 0px 0px 0px;
  min-height: 700px;
  background-color: #F0F7FF;
  position: relative;
  margin-bottom: 50px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.header {
  text-align: center;
  margin-bottom: 60px;
}

.header h2 {
      font-size: 44px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 700;
  color:#1F4E5F;

  margin-bottom: 16px;
}

.subtitle {
 font-size: 20px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 400;
  color:#1F4E5F;
  max-width: 700px;
  margin: 0 auto;
}

/* Cards Grid */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 30px;
}

.card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
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
font-size: 23px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color:#333333;
  margin-bottom: 12px;
}

.card-content p {
  font-size: 16px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 400;
  color:#333333;
  margin-bottom: 20px;
}

.card-btn {
    font-size: 16px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color:white;
  background-color: #1F4E5F;
  border: none;
  padding: 16px 24px 16px 24px;
  border-radius: 38px;
  font-weight: 400;
  cursor: pointer;
  transition: 0.3s;
}

.card-btn:hover {
  background-color: #1F4E5F;;
}
/* Responsive */
@media (max-width: 768px) {
  .header h2 {
    font-size: 2.2rem;
  }
  .imagine-text {
    font-size: 2.3rem;
  }
  .cards-grid {
    grid-template-columns: 1fr;
  }
}
</style>
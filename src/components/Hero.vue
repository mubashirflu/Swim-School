<template>
  <section class="hero">
    <!-- Background Image with Dark Overlay -->
    <div class="hero-bg"></div>

    <div class="hero-content">
      <h1 class="hero-title">From Fear to Freedom<br />in the Water</h1>

      <div class="hero-description">
        <ul>
          <li>You Don't Have To Stay In The Shallow End.</li>
          <li>You Don't Have To Sit Poolside While Everyone Else Jumps In.</li>
          <li>You Deserve To Feel Calm, Capable, And Free In The Water.</li>
        </ul>
      </div>

      <div class="hero-buttons">
        <button class="btn-primary">Book A Free Call</button>
        <button class="btn-secondary">Explore Swim Sessions</button>
      </div>
    </div>

    <!-- Floating Card -->
    <div class="floating-card">
      <div class="card-header">
        Floating And<br />Body Awareness
        <span class="arrow">↗</span>
      </div>
      <img
        src="@/assets/Modern Architectural Structure at Dusk.png"
        alt="Swimmer"
        class="card-image"
      />
    </div>

  </section>
</template>

<script setup>
// You can add any JS logic here later
</script>

<style scoped>
.hero {
  position: relative;
  height: 90vh;           /* ← Height thodi kam ki */
  min-height: 700px;      /* ← Better minimum height */
  overflow: hidden;
  color: white;
  font-family: "DM Sans", sans-serif;
}

.hero-bg {
  position: absolute;
  inset: 0;
  background:
    linear-gradient(rgba(10, 37, 64, 0.65), rgba(10, 37, 64, 0.75)),
    url("@/assets/tropical-palm-luxury-tree-blue.png") center/cover no-repeat;
  z-index: 1;
}

/* Content */
.hero-content {
  position: relative;
  z-index: 2;
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 100px; 
}

.hero-title {
  font-size: 60px;
  font-family: 'DM Sans', sans-serif;
  line-height: 1.1;
  font-weight: 600;
  margin-bottom: 2rem;
  max-width: 800px;
}

.hero-description ul {
  list-style: none;
  padding: 0;
  margin-bottom: 2.5rem;
}

.hero-description li {
  font-size: 20px;
  font-family: 'DM Sans', sans-serif;
  margin-bottom: 0.8rem;
  padding-left: 1.2rem;
  position: relative;
  color: #F5F5F5;
}

.hero-description li::before {
  content: "•";
  color: #F5F5F5;
  position: absolute;
  left: 0;
}

/* Buttons */
.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn-primary {
  background: #4FAFCF;
  color: white;
  font-family: 'DM Sans', sans-serif;
  padding: 16px 24px;
  border-radius: 38px;
  font-weight: 600;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid white;
  padding: 16px 24px;
  border-radius: 38px;
  font-weight: 500;
  font-size: 16px;
  cursor: pointer;
}

/* Floating Card - Position Improved */
.floating-card {
  position: absolute;
  right: 7%;
  bottom: 20%;           /* ← Better position */
  background: #f5f5f530;
  color: white;
  font-family: 'DM Sans', sans-serif;
  border-radius: 16px;
  font-weight: 300;
  width: 260px;
  overflow: hidden;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
  z-index: 3;
}

.card-header {
  padding: 1rem 1.2rem;
  font-weight: 600;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 1.1rem;
  line-height: 1.3;
}

.arrow {
  font-size: 1.5rem;
}

.card-image {
  width: 100%;
  height: 180px;
  object-fit: cover;
}

/* Responsive */
@media (max-width: 1024px) {
  .hero-title {
    font-size: 48px;
  }
  .floating-card {
    right: 5%;
    width: 240px;
    bottom: 10%;
  }
}

@media (max-width: 768px) {
  .hero {
    height: 100vh;
    min-height: 680px;
  }
  .floating-card {
    display: none;   /* Small screen pe floating card hide (optional) */
  }
}
</style>
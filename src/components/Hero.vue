<template>
  <section class="hero">
    <!-- Background Image with Dark Overlay -->
    <div class="hero-bg"></div>

    <div class="hero-content">
      <h1 class="hero-title">
        From Fear to Freedom<br />in the Water
      </h1>

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
// Future JS logic
</script>

<style scoped>

/* ================= HERO ================= */
.hero {
  position: relative;
  height: 100vh;
  min-height: 650px;
  overflow: hidden;
  color: white;
  font-family: "DM Sans", sans-serif;
}

/* ================= BACKGROUND ================= */
.hero-bg {
  position: absolute;
  inset: 0;
  background:
    linear-gradient(rgba(10, 37, 64, 0.68), rgba(10, 37, 64, 0.78)),
    url("@/assets/tropical-palm-luxury-tree-blue.png") center center / cover no-repeat;
  z-index: 1;
}

/* ================= CONTENT ================= */
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

  padding-top: 50px;
  padding-bottom: 40px;
}

.hero-title {
  font-size: clamp(34px, 5vw, 56px);
  line-height: 1.1;
  font-weight: 700;
  margin-bottom: 1.5rem;
  max-width: 820px;
}

.hero-description ul {
  list-style: none;
  padding: 0;
  margin-bottom: 2rem;
}

.hero-description li {
  font-size: clamp(15px, 2vw, 18px);
  margin-bottom: 0.8rem;
  padding-left: 1.4rem;
  position: relative;
  color: #f0f0f0;
}

.hero-description li::before {
  content: "•";
  color: #60b8ff;
  position: absolute;
  left: 0;
  font-size: 1.4em;
}

/* ================= BUTTONS ================= */
.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn-primary,
.btn-secondary {
  font-family: 'DM Sans', sans-serif;
  padding: 15px 26px;
  border-radius: 38px;
  font-weight: 600;
  font-size: 15px;
  cursor: pointer;
  transition: all 0.3s ease;
  white-space: nowrap;
}

.btn-primary {
  background: #4FAFCF;
  color: white;
  border: none;
}

.btn-primary:hover {
  background: #3a9bb8;
  transform: translateY(-3px);
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-3px);
}

/* ================= FLOATING CARD ================= */
.floating-card {
  position: absolute;
  right: 6%;
  bottom: 18%;
  background: rgba(255, 255, 255, 0.12);
  backdrop-filter: blur(12px);
  color: white;
  border-radius: 18px;
  width: 280px;
  overflow: hidden;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.35);
  z-index: 3;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.card-header {
  padding: 1rem 1.2rem;
  font-weight: 600;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 1.1rem;
}

.arrow {
  font-size: 1.5rem;
}

.card-image {
  width: 100%;
  height: 190px;
  object-fit: cover;
}

/* ================= RESPONSIVE ================= */

/* Laptop + Tablet: hide floating card */
@media (max-width: 1024px) {
  .floating-card {
    display: none;
  }
}

/* Tablet / Mobile */
@media (max-width: 768px) {
  .hero-content {
    padding-top: 70px;
    padding-bottom: 30px;
    text-align: left;
    align-items: flex-start;
  }

  .hero-title {
    font-size: 30px;
  }

  .hero-description li {
    font-size: 14px;
  }

  .hero-buttons {
    justify-content: flex-start;
  }
}

/* Small Mobile */
@media (max-width: 480px) {
  .hero-title {
    font-size: 27px;
  }

  .hero-description li {
    font-size: 13.5px;
  }

  .btn-primary,
  .btn-secondary {
    padding: 13px 18px;
    font-size: 14px;
  }
}

</style>
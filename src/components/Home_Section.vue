<template>
  <section class="home-section">
    <div class="container">
      <div class="content-wrapper">

        <!-- LEFT: IMAGE -->
        <div class="images-container">
          <div class="bottom-image">
            <img 
              src="@/assets/Group 1.png" 
              alt="Adult and kids learning to swim"
            />
          </div>
        </div>

        <!-- RIGHT: TEXT -->
        <div class="text-content">
          <h2>If This Sounds Like You...</h2>
          <h3>You’re Not Alone</h3>

          <ul class="bullet-points">
            <li>You’ve avoided pools for years.</li>
            <li>You feel embarrassed you never learned.</li>
            <li>Deep water makes your chest tighten.</li>
            <li>You don’t know how to breathe or float.</li>
            <li>Want to enjoy vacations, family time, and pool days but fear holds you back.</li>
          </ul>

          <p class="description">
            Many adults carry shame around swimming. Many kids feel overwhelmed and misunderstood in traditional lessons. 
            This is a judgment-free space.
          </p>

          <button class="cta-button">
            It’s Okay To Start Now
          </button>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeSection'
}
</script>

<style scoped>

/* ================= BASE ================= */
.home-section {
  background: #F8FAFC;
  padding: 60px 20px;
}

.container {
  max-width: 1280px;
  margin: 0 auto;
}

/* ================= LAYOUT ================= */
.content-wrapper {
  display: flex;
  gap: 70px;
  align-items: center;
  justify-content: space-between;
}

/* ================= IMAGE ================= */
.images-container {
  flex: 1;
  min-width: 0;
}

.bottom-image {
  width: 100%;
  border-radius: 16px;
  overflow: hidden;
}

.images-container img {
  width: 100%;
  height: auto;
  display: block;
}

/* ================= TEXT ================= */
.text-content {
  flex: 1;
  min-width: 0;
}

.text-content h2,
.text-content h3 {
  font-size: 44px;
  font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color: #1F4E5F;
  margin-bottom: 10px;
  line-height: 1.1;
}

.bullet-points {
  list-style: none;
  padding: 0;
  margin-bottom: 20px;
}

.bullet-points li {
  font-size: 16px;
  font-family: 'DM Sans', sans-serif;
  color: #444;
  margin-bottom: 10px;
  padding-left: 15px;
  position: relative;
  line-height: 1.5;
}

.bullet-points li::before {
  content: "•";
  position: absolute;
  left: 0;
  color: #444;
  font-size: 1.3rem;
}

.description {
  font-size: 16px;
  font-family: 'DM Sans', sans-serif;
  color: #444;
  line-height: 1.7;
  margin-bottom: 25px;
}

/* ================= BUTTON ================= */
.cta-button {
  background-color: #1F4E5F;
  color: white;
  border: none;
  padding: 14px 24px;
  font-size: 16px;
  font-family: 'DM Sans', sans-serif;
  border-radius: 38px;
  cursor: pointer;
  transition: 0.3s;
}

.cta-button:hover {
  background-color: #1C89AD;
  transform: translateY(-2px);
}

/* ================= RESPONSIVE ================= */

/* Tablet */
@media (max-width: 1024px) {
  .content-wrapper {
    gap: 40px;
  }

  .text-content h2,
  .text-content h3 {
    font-size: 36px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .content-wrapper {
    flex-direction: column;
    text-align: left;
    gap: 30px;
  }

  .text-content h2,
  .text-content h3 {
    font-size: 30px;
  }

  .bullet-points li {
    font-size: 14px;
  }

  .description {
    font-size: 14px;
  }
}

/* Small Mobile */
@media (max-width: 480px) {
  .home-section {
    padding: 40px 15px;
  }

  .text-content h2,
  .text-content h3 {
    font-size: 26px;
  }

  .cta-button {
    width: 100%;
    text-align: center;
  }
}

/* ================= 320px FIX (IMPORTANT) ================= */
@media (max-width: 360px) {
  .home-section {
    padding: 30px 12px;
  }

  .content-wrapper {
    gap: 20px;
  }

  .text-content h2,
  .text-content h3 {
    font-size: 22px;
    line-height: 1.2;
  }

  .bullet-points li {
    font-size: 13px;
    line-height: 1.4;
  }

  .description {
    font-size: 13px;
    line-height: 1.6;
  }

  .cta-button {
    width: 100%;
    padding: 12px 16px;
    font-size: 14px;
  }
}

</style>
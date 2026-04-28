<template>
  <section class="home-section">
    <div class="container">
      <div class="content-wrapper">
        <div class="images-container">
          <div class="bottom-image">
            <img 
              src="@/assets/Group 1.png" 
              alt="Adult and kids learning to swim"
            />
          </div>
        </div>

        <!-- Right Side Text -->
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
.home-section {
  background: #F8FAFC;
    padding-bottom: 50px;
}

.container {
  max-width: 1280px;
  padding-top: 30px;
  padding-bottom: 50px;
  margin: 0 auto;
}

.content-wrapper {
  display: flex;
  gap: 70px;
  flex-wrap: wrap;
  align-items: flex-start;
}

/* ============== Stacked Images ============== */
.images-container {
  flex: 1;
  min-width: 280px;
  position: relative;
  height: 480px;           /* Container height for stacking */
}

.top-image {
  position: absolute;
  width: 72%;              /* Chhoti size */
  bottom: 30px;            /* Neechay shift kiya */
  right: 0;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
  z-index: 1;
}

.bottom-image {
  position: absolute;
  width: 100%;              /* Thodi aur chhoti */
  top: 40px;               /* Upar shift kiya */
  left: 0;
  border-radius: 16px;
  overflow: hidden;
  /* box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2); */
  /* z-index: 2;              Is image ko upar rakha */
}

.images-container img {
  width: 100%;
  height: auto;
  display: block;
}

/* ============== Text Content ============== */
.text-content {
  flex: 1;
  min-width: 320px;
  padding-top: 20px;
}

.text-content h2 {
  font-size: 44px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color: #1F4E5F;
  margin-bottom: 2px;
}

.text-content h3 {
  font-size: 44px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 600;
  color: #1F4E5F;
  margin-bottom: 25px;
  line-height: 1.1;
}

.bullet-points {
  list-style: none;
  padding: 0;
  margin-bottom: 25px;
}

.bullet-points li {
  font-size: 16px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 400;
  color: #444444;
  margin-bottom: 10px;
  padding-left: 15px;
  position: relative;
}

.bullet-points li::before {
  content: "•";
  position: absolute;
  left: 0;
  color: #444444;
  font-size: 1.4rem;
}

.description {
    font-size: 16px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 400;
  color: #444444;

  line-height: 1.75;
  margin-bottom: 35px;
}

.cta-button {
  background-color: #1F4E5F;
  color: white;
  border: none;
  padding: 16px 24px 16px 24px;
   font-size: 16px;
    font-family: 'DM Sans', sans-serif;
  font-weight: 500;
  border-radius: 38px;
  cursor: pointer;
  transition: 0.3s;
}

.cta-button:hover {
  background-color: #1C89AD8C;
  transform: translateY(-2px);
}

/* Responsive */
@media (max-width: 768px) {
  .images-container {
    height: 420px;
  }
  .content-wrapper {
    gap: 50px;
  }
  .top-image, .bottom-image {
    width: 80%;
  }
}
</style>
<template>
  <header class="header">
    <div class="header-container">

      <!-- Logo -->
      <div class="logo">
        <img src="@/assets/Growing Space Swim.png" alt="Growing Space Swim">
      </div>

      <!-- Navigation -->
      <nav :class="['nav', { active: isMenuOpen }]">
        <a href="#" class="nav-link" @click="closeMenu">Adult Swim Coaching</a>
        <a href="#" class="nav-link" @click="closeMenu">Kids Swim Sessions</a>
        <a href="#" class="nav-link" @click="closeMenu">Clinics</a>
        <a href="#" class="nav-link" @click="closeMenu">About</a>
        <a href="#" class="nav-link" @click="closeMenu">Resources</a>
      </nav>

      <!-- Right Section -->
      <div class="right-section">
        <button class="contact-btn">Contact Us</button>

        <!-- Hamburger -->
        <div class="hamburger" @click="toggleMenu">
          <span :class="{ open: isMenuOpen }"></span>
          <span :class="{ open: isMenuOpen }"></span>
          <span :class="{ open: isMenuOpen }"></span>
        </div>
      </div>

    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<style scoped>

/* =========================
   HEADER
========================= */
.header {
  position: absolute;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  max-width: 1400px;
  z-index: 1000;
  padding: 0 20px;
}

.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: rgba(255, 255, 255, 0.11);
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.25);
  border-radius: 30px;
  padding: 12px 20px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.15);
}

/* LOGO */
.logo img {
  height: 48px;
}

/* NAV */
.nav {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: white;
  text-decoration: none;
  font-size: 16px;
  position: relative;
  transition: 0.3s;
}

.nav-link:hover {
  color: #60b8ff;
}

.nav-link::after {
  content: "";
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: #60b8ff;
  transition: 0.3s;
}

.nav-link:hover::after {
  width: 100%;
}

/* RIGHT */
.right-section {
  display: flex;
  align-items: center;
  gap: 15px;
}

/* BUTTON */
.contact-btn {
  color: white;
  background: rgba(255, 255, 255, 0.11);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 10px 20px;
  border-radius: 30px;
  cursor: pointer;
  transition: 0.3s;
}

.contact-btn:hover {
  background: #4FAFCF;
  color: white;
}

/* HAMBURGER */
.hamburger {
  display: none;
  flex-direction: column;
  cursor: pointer;
  z-index: 1100;
}

.hamburger span {
  width: 25px;
  height: 3px;
  background: white;
  margin: 4px 0;
  transition: 0.3s;
}

/* CROSS ANIMATION */
.hamburger span.open:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.hamburger span.open:nth-child(2) {
  opacity: 0;
}

.hamburger span.open:nth-child(3) {
  transform: rotate(-45deg) translate(6px, -6px);
}

/* =========================
   TABLET (≤1024px)
========================= */
@media (max-width: 1024px) {
  .nav {
    gap: 1.2rem;
  }
}

/* =========================
   DROPDOWN + HAMBURGER (≤900px)
========================= */
@media (max-width: 900px) {

  .nav {
    position: absolute;
    top: 80px;
    left: 0;
    width: 100%;

    flex-direction: column;
    align-items: flex-start;

    background: rgba(10, 37, 64, 0.95);
    backdrop-filter: blur(18px);

    padding: 20px 25px;
    border-radius: 0 0 20px 20px;

    display: flex;
    opacity: 0;
    transform: translateY(-20px);
    pointer-events: none;

    transition: all 0.3s ease;
  }

  .nav.active {
    opacity: 1;
    transform: translateY(0);
    pointer-events: auto;
  }

  .nav-link {
    width: 100%;
    padding: 14px 0;
    font-size: 17px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }

  .nav-link:last-child {
    border-bottom: none;
  }

  .hamburger {
    display: flex;
  }

  .contact-btn {
    display: none;
  }
}

</style>
<template>
  <header class="header">
    <div class="header-container">
      <!-- Logo -->
      <div class="logo">
        <img src="@/assets/Growing Space Swim.png" alt="Growing Space Swim">
      </div>

      <!-- Navigation -->
      <nav class="nav">
        <a href="#" class="nav-link">Adult Swim Coaching</a>
        <a href="#" class="nav-link">Kids Swim Sessions</a>
        <a href="#" class="nav-link">Clinics</a>
        <a href="#" class="nav-link">About</a>
        <a href="#" class="nav-link">Resources</a>
      </nav>

      <!-- Contact Button -->
      <button class="contact-btn">Contact Us</button>
    </div>
  </header>
</template>

<script setup>
</script>

<style scoped>
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
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.25);
  border-radius: 30px;
  padding: 12px 20px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.15);
  max-width: 1320px;
  margin: 0 auto;
}

/* Logo */
.logo img {
  height: 48px;
  width: auto;
  object-fit: contain;
}

/* Navigation */
.nav {
  display: flex;
  align-items: center;
  gap: 2.2rem;
}

.nav-link {
  color: white;
  text-decoration: none;
  font-family: 'DM Sans', system-ui, sans-serif;
  font-weight: 500;
  font-size: 16px;
  transition: all 0.3s ease;
  position: relative;
  white-space: nowrap;
}

.nav-link:hover {
  color: #60b8ff;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: #60b8ff;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

/* Contact Button */
.contact-btn {
  font-family: 'DM Sans', system-ui, sans-serif;
  font-weight: 600;
  font-size: 16px;
  color: white;
  background: rgba(255, 255, 255, 0.11);
  border: 1px solid rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(8px);
  padding: 12px 24px;
  border-radius: 38px;
  cursor: pointer;
  transition: all 0.3s ease;
  white-space: nowrap;
}

.contact-btn:hover {
  background: #60b8ff;
  color: #0a2540;
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(96, 184, 255, 0.3);
}

/* Responsive Design */
@media (max-width: 1024px) {
  .nav {
    gap: 1.8rem;
  }
}

@media (max-width: 768px) {
  .header {
    top: 10px;
    padding: 0 15px;
  }
  
  .header-container {
    padding: 10px 15px;
  }

  .nav {
    display: none; /* You can add hamburger menu later */
  }

  .logo img {
    height: 42px;
  }
}
</style>
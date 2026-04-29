<template>
  <footer class="footer-section">
    <div class="container">
      <div class="footer-content">
        <!-- Top Row -->
        <div class="top-row">
          <div class="left-text">
            <h2 class="main-heading">You’re Right On Time.</h2>
            <p class="sub-text">
              Whether you’re 6 or 60, learning to swim can change how<br>
              you feel about yourself not just in the water, but in life.
            </p>
          </div>

          <button class="clarity-btn" @click="bookClarityCall">
            Book Your Free Clarity Call
          </button>
        </div>

        <!-- Main Footer Links -->
        <div class="footer-links">
          <!-- Reach out -->
          <div class="column">
            <h3 class="column-title">Reach out to us today.</h3>
            <div class="contact-info">
              <p><span class="icon">☎</span> Phone: <a href="tel:(503)998-0902">(503) 998-0902</a></p>
              <p><span class="icon">✉</span> Email: <a href="mailto:grow.in.swim@gmail.com">grow.in.swim@gmail.com</a></p>
              <p><span class="icon">📍</span> Location: Rachael Locke Portland, Oregon</p>
            </div>
          </div>

          <!-- Links -->
          <div class="column">
            <h3 class="column-title">Links</h3>
            <ul>
              <li><a href="#">Home</a></li>
              <li><a href="#">Adult Swim Coaching</a></li>
              <li><a href="#">Kids Swim Sessions</a></li>
              <li><a href="#">Intensive Clinics</a></li>
              <li><a href="#">About Rachael</a></li>
            </ul>
          </div>

          <!-- Legal -->
          <div class="column">
            <h3 class="column-title">Legal</h3>
            <ul>
              <li><a href="#">Pricing & Packages</a></li>
              <li><a href="#">Terms & conditions</a></li>
              <li><a href="#">Privacy policy</a></li>
              <li><a href="#">Cookie policy</a></li>
              <li><a href="#">Contact</a></li>
            </ul>
          </div>
        </div>

        <!-- Bottom Bar -->
        <div class="bottom-bar">
          <p class="copyright">
            © 2026 Growing Space LLC. All Rights Reserved.
          </p>
          
          <div class="social-icons">
            <a href="#" class="social-icon">f</a>
            <a href="#" class="social-icon">📷</a>
            <a href="#" class="social-icon">in</a>
            <a href="#" class="social-icon">𝕏</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterSection',
  methods: {
    bookClarityCall() {
      alert('Opening Free Clarity Call booking...');
      // Add your routing or modal logic here
    }
  }
}
</script>

<style scoped>
.footer-section {
  background: linear-gradient(to bottom, #f8fafc, #e0f2fe);
  padding: 80px 20px 40px;
  font-family: 'DM Sans', sans-serif;
  color: #1e3a8a;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.footer-content {
  border-top: 1px solid #cbd5e1;
  padding-top: 50px;
}

/* Top Row */
.top-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 60px;
  flex-wrap: wrap;
  gap: 30px;
}

.main-heading {
  font-size: 32px;
  font-weight: 700;
  line-height: 1.2;
  margin-bottom: 12px;
  color: #1e3a8a;
}

.sub-text {
  font-size: 17px;
  line-height: 1.65;
  color: #475569;
  max-width: 480px;
}

.clarity-btn {
  background: #1e40af;
  color: white;
  border: none;
  padding: 14px 28px;
  font-size: 1.02rem;
  font-weight: 600;
  border-radius: 50px;
  cursor: pointer;
  white-space: nowrap;
  transition: all 0.3s ease;
  align-self: flex-start;
}

.clarity-btn:hover {
  background: #1e3a8a;
  transform: translateY(-2px);
}

/* Footer Links */
.footer-links {
  display: grid;
  grid-template-columns: 1.8fr 1fr 1fr;
  gap: 40px;
  margin-bottom: 60px;
}

.column-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 18px;
  color: #1e3a8a;
}

.contact-info p {
  margin-bottom: 12px;
  font-size: 15.5px;
  color: #334155;
}

.contact-info a {
  color: #334155;
  text-decoration: none;
}

.contact-info a:hover {
  text-decoration: underline;
}

.footer-links ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-bottom: 10px;
}

.footer-links a {
  color: #475569;
  text-decoration: none;
  font-size: 15.5px;
  transition: color 0.2s;
}

.footer-links a:hover {
  color: #1e40af;
}

/* Bottom Bar */
.bottom-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  padding-top: 30px;
  border-top: 1px solid #e2e8f0;
}

.copyright {
  font-size: 14px;
  color: #64748b;
  margin: 0;
}

.social-icons {
  display: flex;
  gap: 16px;
}

.social-icon {
  width: 36px;
  height: 36px;
  background: rgba(30, 64, 175, 0.1);
  color: #1e40af;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
  text-decoration: none;
  transition: all 0.3s ease;
}

.social-icon:hover {
  background: #1e40af;
  color: white;
  transform: translateY(-2px);
}

/* Responsive */
@media (max-width: 992px) {
  .footer-links {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 640px) {
  .top-row {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .footer-links {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  
  .clarity-btn {
    width: 100%;
    max-width: 320px;
  }
}
</style>
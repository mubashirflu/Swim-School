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
          <div class="links-wrapper">
            <!-- Reach Out -->
            <div class="column contact-column">
              <h3 class="column-title">Reach out to us today.</h3>
              <div class="contact-info">
                <p>
                  <Phone size="20" class="icon" />
                  Phone: <a href="tel:(503)998-0902">(503) 998-0902</a>
                </p>
                <p>
                  <Mail size="20" class="icon" />
                  Email: <a href="mailto:grow.in.swim@gmail.com">grow.in.swim@gmail.com</a>
                </p>
                <p>
                  <MapPin size="20" class="icon" />
                  Location: Rachael Locke Portland, Oregon
                </p>
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
        </div>

        <!-- Bottom Bar -->
        <div class="bottom-bar">
          <p class="copyright">
            © 2026 Growing Space LLC. All Rights Reserved.
          </p>
          
          <div class="social-icons">
            <a href="#" class="social-icon" aria-label="Facebook">
              <Facebook size="20" />
            </a>
            <a href="#" class="social-icon" aria-label="Instagram">
              <Instagram size="20" />
            </a>
            <a href="#" class="social-icon" aria-label="LinkedIn">
              <Linkedin size="20" />
            </a>
            <a href="#" class="social-icon" aria-label="X">
              <Twitter size="20" />
            </a>
          </div>
        </div>

      </div>
    </div>
  </footer>
</template>

<script>
import { Facebook, Instagram, Linkedin, Twitter, Phone, Mail, MapPin } from 'lucide-vue-next'

export default {
  name: 'FooterSection',
  components: {
    Facebook, Instagram, Linkedin, Twitter,
    Phone, Mail, MapPin
  },
  methods: {
    bookClarityCall() {
      alert('Opening Free Clarity Call booking...');
    }
  }
}
</script>

<style scoped>
.footer-section {
  background: #E1F5FB;
  padding: 70px 20px 45px;
  font-family: 'DM Sans', system-ui, sans-serif;
  color: #1e3a8a;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

/* ================= TOP ROW ================= */
.top-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 25px;
  margin-bottom: 45px;
  flex-wrap: wrap;
}

.left-text {
  flex: 1;
  min-width: 260px;
}

.main-heading {
  font-size: 44px;
  font-weight: 700;
  color: #1F4E5F;
  line-height: 1.1;
  margin-bottom: 10px;
}

.sub-text {
  font-size: 16px;
  line-height: 1.6;
  color: #475569;
  max-width: 520px;
}

/* ================= BUTTON FIX ================= */
.clarity-btn {
  background: #1F4E5F;
  color: white;
  border: none;
  padding: 14px 22px;
  font-size: 15px;
  font-weight: 500;
  border-radius: 38px;
  cursor: pointer;
  white-space: nowrap;
  width: fit-content;
  display: inline-block;
  transition: 0.3s ease;
}

.clarity-btn:hover {
  background: #16334d;
  transform: translateY(-2px);
}

/* ================= LINKS ================= */
.footer-links {
  margin-bottom: 35px;
}

.links-wrapper {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 35px;
}

.column-title {
  font-size: 22px;
  font-weight: 600;
  color: #1F4E5F;
  margin-bottom: 14px;
}

.contact-info p {
  margin-bottom: 10px;
  font-size: 15px;
  color: #334155;
  display: flex;
  align-items: center;
  gap: 10px;
}

.footer-links ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-bottom: 8px;
}

.footer-links a {
  color: #475569;
  text-decoration: none;
  font-size: 15px;
}

/* ================= BOTTOM BAR ================= */
.bottom-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
  padding-top: 20px;
  border-top: 1px solid #cbd5e1;
}

.copyright {
  font-size: 14px;
  color: #64748b;
}

.social-icons {
  display: flex;
  gap: 10px;
}

.social-icon {
  width: 36px;
  height: 36px;
  background: rgba(30, 64, 175, 0.08);
  color: #4FAFCF;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: 0.3s ease;
}

.social-icon:hover {
  background: #4FAFCF;
  color: white;
}

/* ================= RESPONSIVE ================= */

/* Tablet */
@media (max-width: 992px) {
  .links-wrapper {
    grid-template-columns: 1fr 1fr;
    gap: 25px;
  }

  .main-heading {
    font-size: 34px;
  }

  .sub-text {
    font-size: 15px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .top-row {
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    margin-bottom: 35px;
  }

  .links-wrapper {
    grid-template-columns: 1fr;
    gap: 22px;
  }

  .main-heading {
    font-size: 28px;
  }

  .sub-text {
    font-size: 14px;
  }

  .bottom-bar {
    flex-direction: column;
    text-align: center;
  }
}

/* Small Mobile */
@media (max-width: 480px) {
  .footer-section {
    padding: 50px 15px 35px;
  }

  .main-heading {
    font-size: 24px;
  }

  .sub-text {
    font-size: 13px;
  }

  .clarity-btn {
    width: auto;
  }
}

/* 320px SAFE */
@media (max-width: 360px) {
  .main-heading {
    font-size: 22px;
  }

  .sub-text {
    font-size: 12.5px;
  }

  .footer-links a {
    font-size: 13px;
  }

  .social-icon {
    width: 32px;
    height: 32px;
  }
}

</style>
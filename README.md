# wma-project
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Blooming Petals | Flower Shop</title>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      body {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        line-height: 1.6;
        color: #333;
      }

      /* Header */
      header {
        background: #fff;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        position: sticky;
        top: 0;
        z-index: 100;
      }
      .header-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 5%;
      }
      .logo {
        font-size: 1.8rem;
        font-weight: bold;
        color: #2a9d8f;
        display: flex;
        align-items: center;
        gap: 10px;
      }
      nav {
        display: flex;
        align-items: center;
      }
      nav a {
        margin-left: 1.5rem;
        text-decoration: none;
        color: #555;
        font-weight: 500;
        transition: color 0.3s;
      }
      nav a:hover {
        color: #e75480;
      }

      /* Hero */
      .hero {
        background: linear-gradient(
            rgba(255, 255, 255, 0.9),
            rgba(255, 255, 255, 0.8)
          ),
          url("https://images.unsplash.com/photo-1464207687429-7505649dae38?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80")
            center/cover;
        padding: 4rem 1rem;
        text-align: center;
      }
      .hero h2 {
        font-size: 2.5rem;
        color: #2a9d8f;
        margin-bottom: 1rem;
      }
      .hero p {
        max-width: 600px;
        margin: 0 auto 1.5rem;
        color: #555;
        font-size: 1.1rem;
      }
      .btn {
        background: #e75480;
        color: white;
        padding: 0.8rem 2rem;
        border: none;
        border-radius: 30px;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.3s;
        font-weight: 600;
      }
      .btn:hover {
        background: #d43f6e;
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      }

      /* Products */
      .section-title {
        text-align: center;
        font-size: 2.2rem;
        color: #2a9d8f;
        margin: 3rem 0 2rem;
        padding-top: 20px;
      }
      .products {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1.5rem;
        padding: 0 5% 3rem;
      }
      .product {
        background: white;
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        transition: 0.3s;
      }
      .product:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
      }
      .product-img {
        height: 200px;
        overflow: hidden;
      }
      .product-img img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 0.5s;
      }
      .product:hover .product-img img {
        transform: scale(1.05);
      }
      .product-info {
        padding: 1.2rem;
      }
      .product-info h3 {
        color: #2a9d8f;
        margin-bottom: 0.5rem;
        font-size: 1.4rem;
      }
      .product-info p {
        color: #666;
        margin-bottom: 1rem;
        font-size: 0.95rem;
      }
      .price {
        color: #e75480;
        font-weight: bold;
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
        display: block;
      }

      /* About */
      .about {
        background: #f9f7f7;
        padding: 3rem 5%;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        gap: 2rem;
      }
      .about-text {
        flex: 1;
        min-width: 300px;
      }
      .about-img {
        flex: 1;
        min-width: 300px;
        border-radius: 10px;
        overflow: hidden;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      }
      .about-img img {
        width: 100%;
        height: auto;
        display: block;
      }

      /* Contact */
      .contact {
        padding: 3rem 5%;
      }
      .contact h3 {
        color: #2a9d8f;
        margin-bottom: 1rem;
        font-size: 1.5rem;
      }
      .contact-container {
        display: flex;
        flex-wrap: wrap;
        gap: 2rem;
      }
      .contact-form {
        flex: 1;
        min-width: 300px;
        background: white;
        padding: 1.5rem;
        border-radius: 10px;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      }
      .form-group {
        margin-bottom: 1rem;
      }
      .form-control {
        width: 100%;
        padding: 0.8rem;
        border: 1px solid #ddd;
        border-radius: 5px;
        font-family: inherit;
        font-size: 1rem;
      }
      .form-control:focus {
        outline: none;
        border-color: #2a9d8f;
      }
      textarea.form-control {
        min-height: 120px;
        resize: vertical;
      }

      /* Contact Info */
      .contact-info {
        flex: 1;
        min-width: 300px;
      }
      .contact-info p {
        margin-bottom: 0.8rem;
        display: flex;
        align-items: center;
        gap: 10px;
      }
      .contact-info i {
        color: #e75480;
        width: 20px;
      }

      /* Footer */
      footer {
        background: #2a9d8f;
        color: white;
        padding: 2rem 5%;
        text-align: center;
      }
      .footer-logo {
        font-size: 1.8rem;
        font-weight: bold;
        margin-bottom: 0.5rem;
      }
      .social-icons {
        margin: 1rem 0;
      }
      .social-icons a {
        color: white;
        margin: 0 0.5rem;
        font-size: 1.2rem;
        transition: all 0.3s;
      }
      .social-icons a:hover {
        color: #e75480;
        transform: translateY(-3px);
      }

      /* Responsive */
      @media (max-width: 768px) {
        .header-container {
          flex-direction: column;
          padding: 1rem;
        }
        nav {
          margin-top: 1rem;
          width: 100%;
          justify-content: center;
          flex-wrap: wrap;
        }
        nav a {
          margin: 0.5rem;
          font-size: 0.9rem;
        }
        .hero h2 {
          font-size: 2rem;
          padding: 0 1rem;
        }
        .hero p {
          padding: 0 1rem;
        }
        .section-title {
          font-size: 1.8rem;
          padding: 0 1rem;
        }
        .products {
          padding: 0 1rem 3rem;
        }
        .about,
        .contact {
          padding: 2rem 1rem;
        }
        .contact-form {
          padding: 1rem;
        }
      }
    </style>
  </head>
  <body>
    <!-- Header -->
    <header>
      <div class="header-container">
        <div class="logo"><i class="fas fa-seedling"></i> Blooming Petals</div>
        <nav>
          <a href="#home">Home</a>
          <a href="#products">Flowers</a>
          <a href="#about">About</a>
          <a href="#contact">Contact</a>
          <a href="#"><i class="fas fa-shopping-cart"></i></a>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
      <h2>Beautiful Flowers for Every Occasion</h2>
      <p>
        Fresh floral arrangements delivered with care. Bringing nature's beauty
        to your doorstep.
      </p>
      <button class="btn">Shop Now</button>
    </section>

    <!-- Products -->
    <section id="products">
      <h2 class="section-title">Featured Flowers</h2>
      <div class="products">
        <div class="product">
          <div class="product-img">
            <img src="download (1).jpg" alt="Rose Bouquet" />
          </div>
          <div class="product-info">
            <h3>Rose Bouquet</h3>
            <p>Elegant red roses perfect for special occasions</p>
            <span class="price">$49.99</span>
            <button
              class="btn"
              style="margin-top: 0; padding: 0.6rem 1.2rem; font-size: 0.9rem"
            >
              Add to Cart
            </button>
          </div>
        </div>

        <div class="product">
          <div class="product-img">
            <img
              src="https://images.unsplash.com/photo-1519378058457-4c29a0a2efac?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80"
              alt="Spring Mix"
            />
          </div>
          <div class="product-info">
            <h3>Spring Mix</h3>
            <p>Vibrant seasonal flowers</p>
            <span class="price">$39.99</span>
            <button
              class="btn"
              style="margin-top: 0; padding: 0.6rem 1.2rem; font-size: 0.9rem"
            >
              Add to Cart
            </button>
          </div>
        </div>

        <div class="product">
          <div class="product-img">
            <img
              src="https://images.unsplash.com/photo-1468327768560-75b778cbb551?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80"
              alt="Orchid"
            />
          </div>
          <div class="product-info">
            <h3>Orchid Plant</h3>
            <p>Elegant potted orchid</p>
            <span class="price">$34.99</span>
            <button
              class="btn"
              style="margin-top: 0; padding: 0.6rem 1.2rem; font-size: 0.9rem"
            >
              Add to Cart
            </button>
          </div>
        </div>

        <div class="product">
          <div class="product-img">
            <img src="download.jpg" alt="Sunflowers" />
          </div>
          <div class="product-info">
            <h3>Sunflowers</h3>
            <p>Bright and cheerful sunflowers</p>
            <span class="price">$29.99</span>
            <button
              class="btn"
              style="margin-top: 0; padding: 0.6rem 1.2rem; font-size: 0.9rem"
            >
              Add to Cart
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
      <div class="about-text">
        <h2 class="section-title">Our Story</h2>
        <p>
          Since 2010, Blooming Petals has been creating beautiful floral
          arrangements for our community. We source fresh flowers daily from
          sustainable growers.
        </p>
        <p>
          Our talented designers create custom arrangements for weddings,
          events, and everyday occasions. Let us help you express your feelings
          through flowers.
        </p>
        <button class="btn" style="margin-top: 1rem">Learn More</button>
      </div>
      <div class="about-img">
        <img
          src="https://images.unsplash.com/photo-1447933601403-0c6688de566e?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80"
          alt="Flower Shop"
        />
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
      <h2 class="section-title">Contact Us</h2>
      <div class="contact-container">
        <div class="contact-form">
          <h3>Send a Message</h3>
          <form id="contactForm">
            <div class="form-group">
              <input
                type="text"
                class="form-control"
                placeholder="Your Name"
                required
              />
            </div>
            <div class="form-group">
              <input
                type="email"
                class="form-control"
                placeholder="Your Email"
                required
              />
            </div>
            <div class="form-group">
              <textarea
                class="form-control"
                placeholder="Your Message"
                rows="4"
                required
              ></textarea>
            </div>
            <button type="submit" class="btn">Send Message</button>
          </form>
        </div>
        <div class="contact-info">
          <h3>Visit Our Shop</h3>
          <p>
            <i class="fas fa-map-marker-alt"></i> 123 Blossom Street, Floraltown
          </p>
          <p><i class="fas fa-phone"></i> (555) 123-4567</p>
          <p><i class="fas fa-envelope"></i> hello@bloomingpetals.com</p>
          <p><i class="fas fa-clock"></i> Mon-Sat: 9am-7pm</p>
          <p><i class="fas fa-truck"></i> Free delivery on orders over $75</p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <div class="footer-logo">Blooming Petals</div>
      <p>Bringing nature's beauty to your doorstep</p>
      <div class="social-icons">
        <a href="#"><i class="fab fa-facebook"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="#"><i class="fab fa-pinterest"></i></a>
      </div>
      <p style="margin-top: 1rem; font-size: 0.9rem; opacity: 0.9">
        &copy; 2023 Blooming Petals. All rights reserved.
      </p>
    </footer>

    <script>
      // Cart functionality
      document.addEventListener("DOMContentLoaded", function () {
        // Add to cart buttons
        const cartButtons = document.querySelectorAll(".btn");
        cartButtons.forEach((button) => {
          if (button.textContent.includes("Add to Cart")) {
            button.addEventListener("click", function () {
              const productName =
                this.parentElement.querySelector("h3").textContent;
              const price =
                this.parentElement.querySelector(".price").textContent;

              // Create a notification
              const notification = document.createElement("div");
              notification.style.cssText = `
                            position: fixed;
                            top: 20px;
                            right: 20px;
                            background: #2a9d8f;
                            color: white;
                            padding: 15px 20px;
                            border-radius: 5px;
                            z-index: 1000;
                            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
                            animation: slideIn 0.3s ease;
                        `;
              notification.innerHTML = `
                            <i class="fas fa-check-circle" style="margin-right: 10px;"></i>
                            Added ${productName} (${price}) to cart!
                        `;
              document.body.appendChild(notification);

              // Remove notification after 3 seconds
              setTimeout(() => {
                notification.style.animation = "slideOut 0.3s ease";
                setTimeout(() => {
                  document.body.removeChild(notification);
                }, 300);
              }, 3000);

              // Button animation
              this.style.backgroundColor = "#2a9d8f";
              setTimeout(() => {
                this.style.backgroundColor = "#e75480";
              }, 300);
            });
          }
        });

        // Form submission
        const contactForm = document.getElementById("contactForm");
        if (contactForm) {
          contactForm.addEventListener("submit", function (e) {
            e.preventDefault();

            // Get form values
            const name = this.querySelector('input[type="text"]').value;
            const email = this.querySelector('input[type="email"]').value;

            // Show success message
            alert(
              `Thank you, ${name}! We have received your message and will respond to ${email} soon.`
            );

            // Reset form
            this.reset();
          });
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a[href^="#"]').forEach((anchor) => {
          anchor.addEventListener("click", function (e) {
            e.preventDefault();
            const targetId = this.getAttribute("href");
            if (targetId === "#") return;

            const targetElement = document.querySelector(targetId);
            if (targetElement) {
              window.scrollTo({
                top: targetElement.offsetTop - 80,
                behavior: "smooth",
              });
            }
          });
        });

        // Add CSS for animations
        const style = document.createElement("style");
        style.textContent = `
                @keyframes slideIn {
                    from { transform: translateX(100%); opacity: 0; }
                    to { transform: translateX(0); opacity: 1; }
                }
                @keyframes slideOut {
                    from { transform: translateX(0); opacity: 1; }
                    to { transform: translateX(100%); opacity: 0; }
                }
            `;
        document.head.appendChild(style);
      });
    </script>
  </body>
</html>

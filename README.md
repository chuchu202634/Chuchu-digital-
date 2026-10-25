
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="My professional portfolio in computing, web development, and digital technology.">
  <title>My Portfolio | Computing Professional</title>

  <style>
    /* GENERAL SETTINGS */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --primary: #38bdf8;
      --dark: #07111f;
      --card: #101e30;
      --text: #e5edf7;
      --muted: #9caec3;
    }

    body {
      font-family: Arial, sans-serif;
      background: var(--dark);
      color: var(--text);
      line-height: 1.7;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1100px, 90%);
      margin: auto;
    }

    /* NAVIGATION */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(7, 17, 31, 0.95);
      border-bottom: 1px solid #203047;
    }

    nav {
      min-height: 75px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
    }

    .logo {
      font-size: 25px;
      font-weight: bold;
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 25px;
      list-style: none;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    .menu-btn {
      display: none;
      font-size: 27px;
      color: white;
      background: none;
      border: none;
      cursor: pointer;
    }

    /* HERO SECTION */
    .hero {
      min-height: 85vh;
      display: flex;
      align-items: center;
      padding: 75px 0;
    }

    .hero-content {
      display: grid;
      grid-template-columns: 1.3fr 1fr;
      gap: 50px;
      align-items: center;
    }

    .tag {
      color: var(--primary);
      font-weight: bold;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    h1 {
      font-size: clamp(38px, 6vw, 65px);
      line-height: 1.15;
      margin: 20px 0;
    }

    h1 span,
    .accent {
      color: var(--primary);
    }

    .hero p,
    .section-description {
      color: var(--muted);
      max-width: 600px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 30px;
    }

    .btn {
      padding: 12px 23px;
      border-radius: 8px;
      background: var(--primary);
      color: #07111f;
      font-weight: bold;
      border: 1px solid var(--primary);
      transition: 0.3s;
      cursor: pointer;
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 25px #38bdf833;
    }

    .btn-outline {
      background: transparent;
      color: var(--primary);
    }

    /* PROFILE CARD */
    .profile-card {
      background: linear-gradient(145deg, #132942, #0c1728);
      border: 1px solid #263b54;
      padding: 35px;
      border-radius: 22px;
      text-align: center;
      box-shadow: 0 20px 50px #0004;
    }

    .avatar {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      margin: 0 auto 20px;
      display: grid;
      place-items: center;
      font-size: 55px;
      font-weight: bold;
      color: var(--primary);
      background: #1b344e;
      border: 3px solid var(--primary);
    }

    .profile-card p {
      margin-top: 8px;
      color: var(--muted);
    }

    .status {
      display: inline-block;
      margin-top: 20px;
      color: #86efac;
      font-size: 14px;
    }

    /* SECTIONS */
    section {
      padding: 85px 0;
      scroll-margin-top: 75px;
    }

    .section-title {
      font-size: 36px;
      margin-bottom: 12px;
    }

    .section-heading {
      margin-bottom: 35px;
    }

    .section-description {
      margin-top: 10px;
    }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 35px;
      align-items: start;
    }

    .info-card,
    .skill-card,
    .project-card,
    .contact-card {
      background: var(--card);
      border: 1px solid #23364d;
      border-radius: 14px;
      padding: 25px;
    }

    .info-card h3,
    .project-card h3 {
      margin-bottom: 12px;
    }

    .info-card p,
    .project-card p {
      color: var(--muted);
    }

    /* SKILLS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .skill-card {
      transition: 0.3s;
    }

    .skill-card:hover,
    .project-card:hover {
      transform: translateY(-5px);
      border-color: var(--primary);
    }

    .skill-icon {
      font-size: 32px;
      margin-bottom: 10px;
    }

    .skill-card p {
      color: var(--muted);
      font-size: 14px;
      margin-top: 8px;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .project-card {
      transition: 0.3s;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }

    .project-number {
      font-size: 34px;
      font-weight: bold;
      color: var(--primary);
      margin-bottom: 10px;
    }

    .project-card p {
      margin-bottom: 18px;
    }

    .project-link {
      color: var(--primary);
      font-weight: bold;
      margin-top: auto;
    }

    /* CONTACT */
    .contact-grid {
      display: grid;
      grid-template-columns: 0.8fr 1.2fr;
      gap: 25px;
    }

    .contact-card p {
      color: var(--muted);
      margin: 10px 0;
      overflow-wrap: anywhere;
    }

    form {
      display: grid;
      gap: 15px;
    }

    input,
    textarea {
      width: 100%;
      padding: 14px;
      border: 1px solid #344960;
      border-radius: 8px;
      background: #091523;
      color: white;
      font: inherit;
    }

    input:focus,
    textarea:focus {
      outline: 2px solid var(--primary);
    }

    textarea {
      resize: vertical;
      min-height: 130px;
    }

    #form-message {
      color: var(--primary);
      overflow-wrap: anywhere;
    }

    /* FOOTER */
    footer {
      padding: 25px 0;
      text-align: center;
      border-top: 1px solid #203047;
      color: var(--muted);
    }

    /* RESPONSIVE DESIGN */
    @media (max-width: 800px) {
      .hero-content,
      .about-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .skills-grid,
      .projects-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .hero {
        min-height: auto;
      }

      .profile-card {
        max-width: 450px;
        width: 100%;
        margin: auto;
      }
    }

    @media (max-width: 600px) {
      .menu-btn {
        display: block;
      }

      .nav-links {
        display: none;
        position: absolute;
        top: 75px;
        left: 0;
        width: 100%;
        padding: 25px;
        background: var(--dark);
        flex-direction: column;
        border-bottom: 1px solid #203047;
      }

      .nav-links.active {
        display: flex;
      }

      .skills-grid,
      .projects-grid {
        grid-template-columns: 1fr;
      }

      .section-title {
        font-size: 29px;
      }

      section {
        padding: 60px 0;
      }

      .profile-card {
        padding: 25px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <header>
    <nav class="container">
      <a href="#home" class="logo">MyPortfolio.</a>

      <button class="menu-btn"
              id="menu-btn"
              aria-label="Toggle navigation"
              aria-expanded="false"
              aria-controls="nav-links">☰</button>

      <ul class="nav-links" id="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <!-- HOME -->
    <section class="hero" id="home">
      <div class="container hero-content">
        <div>
          <span class="tag">Welcome to my portfolio</span>

          <h1>Hello, I'm <span>Your Name</span></h1>

          <h2>Computing Student &amp; <span class="accent"
              id="typing">Web Developer</span></h2>

          <p>
            I am passionate about technology, software development,
            digital innovation, and creating solutions that help
            people and businesses grow.
          </p>

          <div class="buttons">
            <a href="#projects" class="btn">Explore My Work</a>
            <a href="#contact" class="btn btn-outline">Contact Me</a>
          </div>
        </div>

        <div class="profile-card">
          <div class="avatar">YN</div>
          <h2>Your Name</h2>
          <p>Computing | Web Development | Digital Technology</p>
          <span class="status">● Learning, Building &amp; Growing</span>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="container">
        <div class="section-heading">
          <span class="tag">Get to know me</span>
          <h2 class="section-title">About <span class="accent">Me</span></h2>
          <p class="section-description">
            My journey into technology and digital innovation.
          </p>
        </div>

        <div class="about-grid">
          <div class="info-card">
            <h3>Who Am I?</h3>
            <p>
              I am a computing enthusiast interested in web development,
              software, business technology, and artificial intelligence.
              I enjoy learning new skills and turning ideas into useful
              digital projects.
            </p>
          </div>

          <div class="info-card">
            <h3>My Goals</h3>
            <p>
              My goal is to develop professional technical skills,
              build practical applications, solve real-world problems,
              and contribute to digital transformation and economic growth.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <div class="container">
        <div class="section-heading">
          <span class="tag">What I am learning</span>
          <h2 class="section-title">My <span class="accent">Skills</span></h2>
          <p class="section-description">
            Technologies I use or am developing experience with.
          </p>
        </div>

        <div class="skills-grid">
          <div class="skill-card">
            <div class="skill-icon">🌐</div>
            <h3>HTML</h3>
            <p>Building the structure of web pages.</p>
          </div>

          <div class="skill-card">
            <div class="skill-icon">🎨</div>
            <h3>CSS</h3>
            <p>Designing layouts, colors, animations, and responsive pages.</p>
          </div>

          <div class="skill-card">
            <div class="skill-icon">⚡</div>
            <h3>JavaScript</h3>
            <p>Adding interaction and dynamic behavior to websites.</p>
          </div>

          <div class="skill-card">
            <div class="skill-icon">💻</div>
            <h3>Computing</h3>
            <p>Developing computer skills and understanding digital systems.</p>
          </div>

          <div class="skill-card">
            <div class="skill-icon">🤖</div>
            <h3>Artificial Intelligence</h3>
            <p>Exploring AI tools and practical business applications.</p>
          </div>

          <div class="skill-card">
            <div class="skill-icon">🚀</div>
            <h3>Digital Innovation</h3>
            <p>Exploring ideas that improve services and businesses.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects">
      <div class="container">
        <div class="section-heading">
          <span class="tag">What I am building</span>
          <h2 class="section-title">My <span class="accent">Projects</span></h2>
          <p class="section-description">
            Example project cards. Replace these with your actual work.
          </p>
        </div>

        <div class="projects-grid">
          <article class="project-card">
            <div class="project-number">01</div>
            <h3>Personal Portfolio</h3>
            <p>
              A responsive website introducing my skills, goals,
              and professional work.
            </p>
            <a class="project-link" href="#home">View Portfolio ↑</a>
          </article>

          <article class="project-card">
            <div class="project-number">02</div>
            <h3>CPC Technology</h3>
            <p>
              A sample digital technology project focused on
              presenting services and digital opportunities.
            </p>
            <a class="project-link" href="#contact">Learn More ↑</a>
          </article>

          <article class="project-card">
            <div class="project-number">03</div>
            <h3>Business Website</h3>
            <p>
              A sample website concept for showcasing products,
              services, and business information.
            </p>
            <a class="project-link" href="#contact">Learn More ↑</a>
          </article>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="container">
        <div class="section-heading">
          <span class="tag">Let's connect</span>
          <h2 class="section-title">Contact <span class="accent">Me</span></h2>
          <p class="section-description">
            Have a project idea or want to discuss technology?
            Send me a message.
          </p>
        </div>

        <div class="contact-grid">
          <div class="contact-card">
            <h3>Contact Information</h3>
            <p>Email: your-email@example.com</p>
            <p>Location: Ethiopia</p>
            <p>Interests: Computing, Business &amp; Technology</p>
          </div>

          <div class="contact-card">
            <form id="contact-form">
              <input type="text" id="name"
                     placeholder="Your name" required>

              <input type="email" id="email"
                     placeholder="Your email address" required>

              <textarea id="message"
                        placeholder="Write your message..."
                        required></textarea>

              <button class="btn" type="submit">Prepare Email</button>
              <p id="form-message" aria-live="polite"></p>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- FOOTER -->
  <footer>
    <div class="container">
      <p>© <span id="year"></span> Your Name. Built with HTML, CSS &amp; JavaScript.</p>
    </div>
  </footer>

  <script>
    // MOBILE MENU
    const menuBtn = document.getElementById("menu-btn");
    const navLinks = document.getElementById("nav-links");

    menuBtn.addEventListener("click", () => {
      const isOpen = navLinks.classList.toggle("active");
      menuBtn.setAttribute("aria-expanded", String(isOpen));
    });

    // CLOSE MENU AFTER CLICKING A LINK
    navLinks.querySelectorAll("a").forEach(link => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("active");
        menuBtn.setAttribute("aria-expanded", "false");
      });
    });

    // CURRENT YEAR
    document.getElementById("year").textContent =
      new Date().getFullYear();

    // SIMPLE TYPING ANIMATION
    const typingElement = document.getElementById("typing");
    const words = [
      "Web Developer",
      "Computing Student",
      "Digital Innovator"
    ];

    let wordIndex = 0;
    let letterIndex = 0;
    let deleting = false;

    function typeEffect() {
      const word = words[wordIndex];

      typingElement.textContent = word.substring(0, letterIndex);

      if (!deleting) {
        letterIndex++;

        if (letterIndex > word.length) {
          deleting = true;
          setTimeout(typeEffect, 1200);
          return;
        }
      } else {
        letterIndex--;

        if (letterIndex < 0) {
          deleting = false;
          letterIndex = 0;
          wordIndex = (wordIndex + 1) % words.length;
        }
      }

      setTimeout(typeEffect, deleting ? 45 : 90);
    }

    typeEffect();

    // CONTACT FORM
    // Opens the visitor's email application.
    // This is not an online form submission service.
    document.getElementById("contact-form").addEventListener(
      "submit", function(event) {
        event.preventDefault();

        const name = document.getElementById("name").value.trim();
        const email = document.getElementById("email").value.trim();
        const message = document.getElementById("message").value.trim();
        const status = document.getElementById("form-message");

        if (!name || !email || !message) {
          status.textContent = "Please complete all fields.";
          return;
        }

        // Replace with your real email address.
        const recipient = "your-email@example.com";

        const subject = encodeURIComponent(
          "Portfolio message from " + name
        );

        const body = encodeURIComponent(
          "Name: " + name +
          "\nEmail: " + email +
          "\n\nMessage:\n" + message
        );

        status.textContent =
          "Opening your email application. Please send the prepared message.";

        window.location.href =
          "mailto:" + recipient +
          "?subject=" + subject +
          "&body=" + body;
      }
    );
  </script>
</body>
</html>


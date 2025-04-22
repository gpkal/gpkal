<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Giorgia Prina - GitHub Profile</title>
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      line-height: 1.6;
      color: #24292e;
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
      background-color: #fafafa;
    }
    
    h1, h2, h3 {
      font-weight: 600;
      text-align: center;
    }
    
    h1 {
      font-size: 24px;
      margin-bottom: 8px;
    }
    
    h2 {
      font-size: 18px;
      color: #586069;
      margin-top: 0;
      font-weight: 400;
      margin-bottom: 24px;
    }
    
    h3 {
      font-size: 16px;
      margin-top: 24px;
      margin-bottom: 8px;
      border-bottom: 1px solid #eaecef;
      padding-bottom: 4px;
      text-align: left;
    }
    
    a {
      color: #0366d6;
      text-decoration: none;
    }
    
    a:hover {
      text-decoration: underline;
    }
    
    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      justify-content: center;
    }
    
    .tech-item {
      background-color: #f1f1f1;
      padding: 3px 10px;
      border-radius: 12px;
      font-size: 14px;
    }
    
    .projects {
      margin-top: 16px;
    }
    
    .project {
      margin-bottom: 16px;
    }
    
    .project-title {
      font-weight: 600;
      margin-bottom: 4px;
    }
    
    .connect {
      display: flex;
      gap: 12px;
      margin-top: 16px;
      justify-content: center;
    }
    
    .quote {
      font-style: italic;
      color: #586069;
      padding: 16px 0;
      border-top: 1px solid #eaecef;
      margin-top: 24px;
      text-align: center;
    }
    
    .banner {
      position: relative;
      height: 200px;
      background-color: #f0f0f0;
      margin-bottom: 32px;
      border-radius: 4px;
      overflow: hidden;
    }
    
    .banner-slide {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      padding: 0 32px;
      opacity: 0;
      transition: opacity 0.5s ease;
      text-align: center;
    }
    
    .banner-slide.active {
      opacity: 1;
    }
    
    .banner-title {
      font-size: 18px;
      font-weight: 600;
      margin-bottom: 12px;
    }
    
    .banner-content {
      font-size: 16px;
      line-height: 1.5;
    }
    
    .pagination {
      position: absolute;
      bottom: 16px;
      left: 0;
      right: 0;
      display: flex;
      justify-content: center;
      gap: 8px;
    }
    
    .dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background-color: #ddd;
      cursor: pointer;
    }
    
    .dot.active {
      background-color: #333;
    }
    
    .featured-projects {
      margin-top: 32px;
    }
  </style>
</head>
<body>
  <h1>Giorgia Prina</h1>
  <h2>Data Scientist</h2>
  
  <div class="banner">
    <div class="banner-slide active">
      <div class="banner-title">Education & Tech Passion</div>
      <div class="banner-content">
        MSc in Data Science from University of Milano-Bicocca. Experience in machine learning, deep learning, and data visualization.
      </div>
    </div>
    <div class="banner-slide">
      <div class="banner-title">Personal Interests</div>
      <div class="banner-content">
        Reader of crime, mystery, economics and history books.
        Corgi lover.
        Mountain passionate.
      </div>
    </div>
    <div class="banner-slide">
      <div class="banner-title">Tech Stack</div>
      <div class="tech-stack">
        <span class="tech-item">Python</span>
        <span class="tech-item">SQL</span>
        <span class="tech-item">R</span>
        <span class="tech-item">TensorFlow</span>
        <span class="tech-item">PyTorch</span>
        <span class="tech-item">Scikit-Learn</span>
        <span class="tech-item">Tableau</span>
        <span class="tech-item">Qlik</span>
        <span class="tech-item">MongoDB</span>
        <span class="tech-item">Git</span>
      </div>
    </div>
    <div class="pagination">
      <div class="dot active" onclick="showSlide(0)"></div>
      <div class="dot" onclick="showSlide(1)"></div>
      <div class="dot" onclick="showSlide(2)"></div>
    </div>
  </div>
  
  <h3>Connect</h3>
  <div class="connect">
    <a href="https://www.linkedin.com/in/giorgia-prina/">LinkedIn</a>
    <a href="mailto:giorgiaprina2@gmail.com">Email</a>
    <a href="https://github.com/gpkal">GitHub</a>
  </div>
  
  <div class="quote">
    "cit." — W. AB
  </div>

  <script>
    const slides = document.querySelectorAll('.banner-slide');
    const dots = document.querySelectorAll('.dot');
    let currentSlide = 0;
    
    function showSlide(n) {
      slides.forEach(slide => slide.classList.remove('active'));
      dots.forEach(dot => dot.classList.remove('active'));
      
      slides[n].classList.add('active');
      dots[n].classList.add('active');
      currentSlide = n;
    }
    
    function nextSlide() {
      let next = (currentSlide + 1) % slides.length;
      showSlide(next);
    }
    
    // Auto-rotate slides
    setInterval(nextSlide, 3500);
  </script>
</body>
</html>

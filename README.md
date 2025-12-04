<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ProTopup - Professional Game Top-Up Service</title>
  <meta name="description" content="বাংলাদেশের সবচেয়ে বিশ্বস্ত গেম টপ-আপ সার্ভিস। Free Fire, PUBG, Mobile Legends, Brawl Stars সহ সব গেমের ডায়মন্ড/UC তাৎক্ষণিক ডেলিভারি।"/>
  
  <!-- SEO & OG Tags -->
  <meta property="og:title" content="ProTopup - Professional Game Top-Up Service"/>
  <meta property="og:description" content="সবচেয়ে দ্রুত ও নিরাপদ গেম টপ-আপ সার্ভিস"/>
  <meta property="og:type" content="website"/>
  
  <!-- Favicon -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>💎</text></svg>">
  
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --primary: #2563eb;
      --primary-dark: #1d4ed8;
      --secondary: #64748b;
      --light: #f8fafc;
      --dark: #0f172a;
      --gray-100: #f1f5f9;
      --gray-200: #e2e8f0;
      --gray-300: #cbd5e1;
      --success: #10b981;
    }
    
    * { margin:0; padding:0; box-sizing:border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background:#fff;
      color:#1e293b;
      line-height:1.6;
      transition: all 0.3s;
    }
    body.dark { background:#0f172a; color:#e2e8f0; }
    
    /* Navbar */
    nav {
      background:var(--light);
      box-shadow:0 4px 6px -1px rgba(0,0,0,0.1);
      position:fixed;
      width:100%;
      top:0;
      z-index:1000;
      transition:all 0.3s;
    }
    body.dark nav { background:#1e293b; }
    
    .nav-container {
      max-width:1400px;
      margin:auto;
      padding:1rem;
      display:flex;
      justify-content:space-between;
      align-items:center;
    }
    .logo {
      font-size:1.8rem;
      font-weight:700;
      color:var(--primary);
    }
    .nav-links a {
      margin:0 1.5rem;
      text-decoration:none;
      color:var(--dark);
      font-weight:500;
    }
    body.dark .nav-links a { color:#e2e8f0; }
    .nav-links a:hover { color:var(--primary); }
    
    /* Hero */
    .hero {
      background:linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color:white;
      text-align:center;
      padding:120px 20px 80px;
    }
    .hero h1 {
      font-size:3.5rem;
      margin-bottom:1rem;
    }
    .hero p {
      font-size:1.3rem;
      max-width:800px;
      margin:0 auto 2rem;
    }
    
    /* Top-up Form */
    .container {
      max-width:1200px;
      margin:4rem auto;
      padding:0 20px;
    }
    .card {
      background:white;
      border-radius:12px;
      box-shadow:0 10px 25px rgba(0,0,0,0.1);
      padding:3rem;
      margin-bottom:3rem;
    }
    body.dark .card { background:#1e293b; }
    
    .form-grid {
      display:grid;
      grid-template-columns:repeat(auto-fit, minmax(300px,1fr));
      gap:1.5rem;
    }
    input, select, button {
      width:100%;
      padding:1rem;
      border-radius:8px;
      border:1px solid var(--gray-300);
      font-size:1rem;
    }
    body.dark input, body.dark select { background:#334155; border:none; color:white; }
    
    button {
      background:var(--primary);
      color:white;
      border:none;
      font-weight:600;
      cursor:pointer;
      transition:0.3s;
    }
    button:hover { background:var(--primary-dark); transform:translateY(-2px); }
    
    /* Footer */
    footer {
      background:var(--dark);
      color:white;
      text-align:center;
      padding:3rem 20px;
    }
    body.dark footer { background:#020617; }
    
    /* Dark Mode Toggle */
    .theme-toggle {
      background:none;
      border:none;
      font-size:1.5rem;
      cursor:pointer;
    }
    
    /* Responsive */
    @media (max-width:768px) {
      .hero h1 { font-size:2.5rem; }
      .nav-links { display:none; }
    }
    
    .loading {
      display:none;
      text-align:center;
      padding:3rem;
    }
    .spinner {
      border:4px solid #f3f3f3;
      border-top:4px solid var(--primary);
      border-radius:50%;
      width:50px;
      height:50px;
      animation:spin 1s linear infinite;
      margin:0 auto 1rem;
    }
    @keyframes spin { 0% { transform:rotate(0deg); } 100% { transform:rotate(360deg); } }
  </style>
</head>
<body>
  <nav>
    <div class="nav-container">
      <div class="logo">ProTopup</div>
      <div class="nav-links">
        <a href="#">হোম</a>
        <a href="#">গেম লিস্ট</a>
        <a href="#">কীভাবে কিনবেন</a>
        <a href="#">লগইন</a>
      </div>
      <button class="theme-toggle" onclick="toggleTheme()">🌙</button>
    </div>
  </nav>

  <section class="hero">
    <h1>ProTopup</h1>
    <p>বাংলাদেশের সবচেয়ে বিশ্বস্ত ও দ্রুত গেম টপ-আপ সার্ভিস</p>
    <p>Free Fire • PUBG • Mobile Legends • Valorant • Roblox</p>
  </section>

  <div class="container">
    <div class="card">
      <h2 style="text-align:center;margin-bottom:2rem;">টপ-আপ করুন</h2>
      <div class="form-grid">
        <input type="text" placeholder="গেম আইডি / Player ID" required />
        <select required>
          <option value="">গেম সিলেক্ট করুন</option>
          <option>Free Fire</option>
          <option>PUBG Mobile</option>
          <option>Mobile Legends</option>
          <option>Valorant</option>
        </select>
        <select required>
          <option value="">প্যাকেজ সিলেক্ট করুন</option>
          <option>100 ডায়মন্ড - ৳90</option>
          <option>310 ডায়মন্ড - ৳270</option>
          <option>520 ডায়মন্ড - ৳450</option>
          <option>1075 ডায়মন্ড - ৳900</option>
        </select>
        <select required>
          <option value="">পেমেন্ট মেথড</option>
          <option>bKash</option>
          <option>Nagad</option>
          <option>Rocket</option>
          <option>Upay</option>
        </select>
        <input type="text" placeholder="আপনার মোবাইল নাম্বার" required />
        <button onclick="submitTopup()">পেমেন্ট করুন</button>
      </div>
    </div>

    <div class="loading" id="loading">
      <div class="spinner"></div>
      <p>পেমেন্ট প্রসেসিং হচ্ছে...</p>
    </div>

    <div class="card" id="success" style="display:none;text-align:center;">
      <h2 style="color:var(--success);">পেমেন্ট সফল হয়েছে! 🎉</h2>
      <p>আপনার অ্যাকাউন্টে ডায়মন্ড যোগ হয়ে গেছে।</p>
      <button onclick="location.reload()" style="margin-top:2rem;">নতুন টপ-আপ করুন</button>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 ProTopup - All Rights Reserved</p>
    <p>সাপোর্ট: 018xx-xxxxxx | support@protopup.com</p>
  </footer>

  <script>
    function toggleTheme() {
      document.body.classList.toggle('dark');
      localStorage.setItem('dark', document.body.classList.contains('dark'));
    }
    
    if(localStorage.getItem('dark') === 'true') {
      document.body.classList.add('dark');
    }
    
    function submitTopup() {
      document.querySelector('.card').style.display = 'none';
      document.getElementById('loading').style.display = 'block';
      
      setTimeout(() => {
        document.getElementById('loading').style.display = 'none';
        document.getElementById('success').style.display = 'block';
      }, 3000);
    }
  </script>
</body>
</html># Black-city-
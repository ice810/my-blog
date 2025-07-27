# my-blog
<html lang="en" dir="ltr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Blog - Home</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #121212;
      color: #ffffff;
    }
    header {
      background-color: #1f1f1f;
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 {
      margin: 0;
      font-size: 1.5rem;
    }
    .lang-toggle {
      background: none;
      border: 1px solid #444;
      color: #fff;
      padding: 0.4rem 0.8rem;
      border-radius: 6px;
      cursor: pointer;
    }
    .post {
      background-color: #1e1e1e;
      margin: 1rem;
      padding: 1rem;
      border-radius: 10px;
    }
    .user-info {
      display: flex;
      align-items: center;
      margin-bottom: 0.5rem;
    }
    .user-info img {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      margin-right: 10px;
    }
    .username {
      font-weight: bold;
    }
    .username a {
      color: #4eaaff;
      text-decoration: none;
    }
    .username a:hover {
      text-decoration: underline;
    }
    .post img, .post video {
      width: 100%;
      max-height: 400px;
      border-radius: 10px;
      object-fit: cover;
    }
    .post .caption {
      margin-top: 0.5rem;
      font-size: 1rem;
    }
    @media (max-width: 600px) {
      header h1 {
        font-size: 1.2rem;
      }
      .post .caption {
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1 id="title">My Blog</h1>
    <button class="lang-toggle" onclick="toggleLanguage()">عربي</button>
  </header>

  <!-- Instagram-style photo post by aa.abuwafy -->
  <div class="post">
    <div class="user-info">
      <img src="profile1.jpg" alt="aa.abuwafy">
      <span class="username"><a href="https://www.instagram.com/aa.abuwafy" target="_blank">aa.abuwafy</a></span>
    </div>
    <img src="insta-photo1.jpg" alt="Photo by aa.abuwafy">
    <p class="caption" id="caption1">Chillin' in the city ☀️</p>
  </div>

  <!-- TikTok-style video post by aa_abowafy -->
  <div class="post">
    <div class="user-info">
      <img src="profile2.jpg" alt="aa_abowafy">
      <span class="username"><a href="https://www.tiktok.com/@aa_abowafy" target="_blank">aa_abowafy</a></span>
    </div>
    <video controls>
      <source src="tiktok-video1.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="caption" id="caption2">Fun times with friends! 🎉</p>
  </div>

  <script>
    let isArabic = false;

    function toggleLanguage() {
      isArabic = !isArabic;
      document.getElementById('title').innerText = isArabic ? 'مدونتي' : 'My Blog';
      document.querySelector('.lang-toggle').innerText = isArabic ? 'English' : 'عربي';
      document.getElementById('caption1').innerText = isArabic ? 'استجمام في المدينة ☀️' : "Chillin' in the city ☀️";
      document.getElementById('caption2').innerText = isArabic ? 'أوقات ممتعة مع الأصدقاء! 🎉' : "Fun times with friends! 🎉";
      document.body.setAttribute('dir', isArabic ? 'rtl' : 'ltr');
    }
  </script>
</body>
</html>

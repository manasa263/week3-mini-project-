<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Editkaro.in | Portfolio</title>
  <style>
    /* ===== RESET ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #0f0f0f;
      color: white;
      line-height: 1.6;
    }

    header {
      text-align: center;
      padding: 2rem;
      background: linear-gradient(90deg, #ff416c, #ff4b2b);
    }

    header h1 {
      font-size: 2.5rem;
    }

    .filter-buttons {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      margin: 1rem 0;
      gap: 10px;
    }

    .filter-buttons button {
      background: #ff4b2b;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 25px;
      font-weight: bold;
      transition: 0.3s;
    }

    .filter-buttons button:hover {
      background: #ff416c;
      transform: scale(1.05);
    }

    .portfolio {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      padding: 2rem;
    }

    .video-card {
      background: #1a1a1a;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
      transition: transform 0.3s;
    }

    .video-card:hover {
      transform: translateY(-8px);
    }

    .video-card video {
      width: 100%;
      height: auto;
      display: block;
    }

    .video-info {
      padding: 10px;
      text-align: center;
    }

    .hidden {
      display: none;
    }

    footer {
      text-align: center;
      padding: 1.5rem;
      background: #111;
      margin-top: 2rem;
    }

    footer p {
      font-size: 0.9rem;
      color: #bbb;
    }
  </style>
</head>
<body>

  <header>
    <h1>🎬 Editkaro.in Portfolio</h1>
    <p>Social Media Marketing & Video Editing Agency</p>
  </header>

  <div class="filter-buttons">
    <button onclick="filterVideos('all')">All</button>
    <button onclick="filterVideos('shorts')">Short-form</button>
    <button onclick="filterVideos('long')">Long-form</button>
    <button onclick="filterVideos('gaming')">Gaming</button>
    <button onclick="filterVideos('football')">Football</button>
    <button onclick="filterVideos('ads')">Ads</button>
    <button onclick="filterVideos('anime')">Anime</button>
  </div>

  <section class="portfolio">
    <!-- Example Video Cards -->
    <div class="video-card shorts">
      <video src="videos/short1.mp4" controls poster="thumbnails/short1.jpg"></video>
      <div class="video-info">Short Video 1</div>
    </div>

    <div class="video-card long">
      <video src="videos/long1.mp4" controls poster="thumbnails/long1.jpg"></video>
      <div class="video-info">Long-form Video 1</div>
    </div>

    <div class="video-card gaming">
      <video src="videos/game1.mp4" controls poster="thumbnails/game1.jpg"></video>
      <div class="video-info">Gaming Edit</div>
    </div>

    <div class="video-card football">
      <video src="videos/football1.mp4" controls poster="thumbnails/football1.jpg"></video>
      <div class="video-info">Football Edit</div>
    </div>

    <div class="video-card ads">
      <video src="videos/ad1.mp4" controls poster="thumbnails/ad1.jpg"></video>
      <div class="video-info">Ad Campaign</div>
    </div>

    <div class="video-card anime">
      <video src="videos/anime1.mp4" controls poster="thumbnails/anime1.jpg"></video>
      <div class="video-info">Anime Edit</div>
    </div>
  </section>

  <footer>
    <p>© 2025 Editkaro.in | All Rights Reserved</p>
  </footer>

  <script>
    function filterVideos(category) {
      let videos = document.querySelectorAll(".video-card");
      videos.forEach(video => {
        if (category === "all" || video.classList.contains(category)) {
          video.classList.remove("hidden");
        } else {
          video.classList.add("hidden");
        }
      });
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Flip Up Game</title>

  <!-- Tailwind CSS -->
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <!-- Material Icons -->
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <!-- AOS (Animate On Scroll) -->
  <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">

  <style>
    .goldenrod { color: goldenrod; }
    .bg-goldenrod { background-color: goldenrod; }
    .border-goldenrod { border-color: goldenrod; }

    /* Modal slide-in */
    .slide-in {
      animation: slideIn 0.5s ease-out forwards;
    }

    @keyframes slideIn {
      from {
        transform: translateY(100%);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }
  </style>
</head>
<body class="bg-white font-sans text-gray-800">

  <!-- Hero Section -->
  <section class="relative h-screen bg-cover bg-center text-white" style="background-image: url('https://i.ibb.co/mCGxpQtD/FB-IMG-17369745733970614.jpg');">
    <div class="absolute inset-0 bg-black bg-opacity-60"></div>
    <div class="relative z-10 flex flex-col items-center justify-center h-full text-center px-4">
      <h1 class="text-5xl font-bold mb-4">
        <span class="material-icons text-6xl text-goldenrod align-middle">games</span>
        Flip Up Game
      </h1>
      <p class="text-xl mb-6 text-goldenrod">Memory meets speed. Flip and match to win!</p>
      <div class="flex gap-4">
        <button onclick="toggleModal()" class="bg-goldenrod text-white px-6 py-3 rounded-lg text-lg font-semibold shadow-md hover:opacity-90 transition">
          Start Game
        </button>
        <a href="#" class="border-2 border-white text-white px-6 py-3 rounded-lg text-lg hover:bg-white hover:text-goldenrod transition">
          Leaderboard
        </a>
      </div>
    </div>
  </section>

  <!-- Section 1 - Train Your Brain -->
  <section class="py-20 px-6 md:px-16 bg-white">
    <div class="flex flex-col md:flex-row items-center gap-10">
      <div class="md:w-1/2">
        <h2 class="text-3xl font-bold goldenrod mb-4">
          <span class="material-icons align-middle">psychology</span>
          Train Your Brain
        </h2>
        <p class="text-lg">Every card you flip boosts your brainpower. Challenge your memory and focus with each round.</p>
      </div>
      <img
        data-aos="fade-right"
        data-aos-duration="800"
        src="https://i.ibb.co/YxyL6GC/2024-12-31-12-45-37-6-w-400px-w-650px.jpg"
        alt="Memory Game"
        class="md:w-1/2 rounded shadow-lg"
      />
    </div>
  </section>

  <!-- Section 2 - Score & Earn -->
  <section class="py-20 px-6 md:px-16 bg-gray-50">
    <div class="flex flex-col-reverse md:flex-row items-center gap-10">
      <img
        data-aos="fade-right"
        data-aos-duration="800"
        src="https://i.ibb.co/2PQP1T5/iPhoneX.png"
        alt="Rewards"
        class="md:w-1/2 rounded shadow-lg"
      />
      <div class="md:w-1/2">
        <h2 class="text-3xl font-bold goldenrod mb-4">
          <span class="material-icons align-middle">emoji_events</span>
          Score & Earn
        </h2>
        <p class="text-lg">Higher scores earn you exclusive bonuses. Climb the leaderboard and unlock achievements!</p>
      </div>
    </div>
  </section>

  <!-- Section 3 - Optimized for Mobile -->
  <section class="py-20 px-6 md:px-16 bg-white">
    <div class="flex flex-col md:flex-row items-center gap-10">
      <div class="md:w-1/2">
        <h2 class="text-3xl font-bold goldenrod mb-4">
          <span class="material-icons align-middle">mobile_friendly</span>
          Optimized for Mobile
        </h2>
        <p class="text-lg">Flip Up works best in the app with smooth animations, offline mode, and lightning-fast performance.</p>
      </div>
      <img
        data-aos="fade-right"
        data-aos-duration="800"
        src="https://i.ibb.co/fS12Ctj/api.png"
        alt="Mobile"
        class="md:w-1/2 rounded shadow-lg"
      />
    </div>
  </section>

  <!-- Section 4 - Community -->
  <section class="py-20 px-6 md:px-16 bg-gray-50">
    <div class="flex flex-col-reverse md:flex-row items-center gap-10">
      <img
        data-aos="fade-right"
        data-aos-duration="800"
        src="https://i.ibb.co/VYfDzJjc/5f09e572b2481afafa89d7b917868b7a.png"
        alt="Community"
        class="md:w-1/2 rounded shadow-lg"
      />
      <div class="md:w-1/2">
        <h2 class="text-3xl font-bold goldenrod mb-4">
          <span class="material-icons align-middle">group</span>
          Join the Flip Up Community
        </h2>
        <p class="text-lg">Compete globally, share strategies, and celebrate milestones with fellow gamers.</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-10 text-center text-sm text-gray-500">
    <span class="material-icons align-middle">copyright</span>
    2025 Flip Up Game. All rights reserved.
  </footer>

  <!-- Modal -->
  <div id="appModal" class="fixed inset-0 bg-black bg-opacity-50 hidden items-center justify-center z-50">
    <div class="bg-white rounded-lg p-6 max-w-md w-full text-center slide-in">
      <span class="material-icons text-goldenrod text-5xl mb-4">download_for_offline</span>
      <h2 class="text-2xl font-bold goldenrod mb-2">Better in the App</h2>
      <p class="mb-4">Flip Up is smoother and faster in our mobile app. Download now for the best experience!</p>
      <a href="https://upload.app/download/massive-win/massive.win/45e2bda5ff1ca3896fc3cc0bd4625f33f558ab3eb5350131758c50871c013652" class="bg-goldenrod text-white px-6 py-2 rounded-lg font-semibold hover:opacity-90 transition">Download App</a>
      <br/><br/>
      <button onclick="toggleModal()" class="text-sm text-gray-500 hover:underline">Continue on Web</button>
    </div>
  </div>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, once: true });

    function toggleModal() {
      const modal = document.getElementById('appModal');
      modal.classList.toggle('hidden');
      modal.classList.toggle('flex');
    }
  </script>
</body>
</html>

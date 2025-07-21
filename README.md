# randeeps-birthday<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Randeep's Birthday Invite</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #000000, #1a1a1a);
      color: #f5f5f5;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
    }
    h1 {
      font-size: 2.5rem;
      color: #FFD700;
      margin-bottom: 1rem;
    }
    p {
      font-size: 1.2rem;
      margin: 0.5rem 0;
      text-align: center;
      max-width: 90%;
    }
    .invite-box {
      background-color: rgba(0, 0, 0, 0.85);
      border: 2px solid #FFD700;
      border-radius: 20px;
      padding: 2rem;
      text-align: center;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.4);
    }
    .countdown {
      font-size: 2rem;
      margin-top: 1rem;
      font-weight: bold;
      color: #FF6347;
    }
    .rsvp-btn {
      margin-top: 2rem;
      padding: 0.8rem 1.5rem;
      background-color: #FFD700;
      border: none;
      border-radius: 10px;
      color: black;
      font-weight: bold;
      cursor: pointer;
      font-size: 1rem;
      text-decoration: none;
    }
    .rsvp-btn:hover {
      background-color: #ffc800;
    }
  </style>
</head>
<body>
  <div class="invite-box">
    <h1>You're Invited!</h1>
    <p>Hey, it's me Randeep and I want you to attend my birthday celebration!</p>
    <p>Become part of my big day 🎉</p>
    <p><strong>Date:</strong> July 29, 2025</p>
    <p><strong>Time:</strong> 6 PM to 8 PM</p>
    <p><strong>Venue:</strong> Randeep's House</p>
    <div class="countdown" id="countdown"></div>
    <a class="rsvp-btn" href="https://instagram.com/maverick.rudra" target="_blank">RSVP on Instagram</a>
  </div>
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
  <script>
    const targetDate = new Date("July 29, 2025 18:00:00").getTime();
    const countdownInterval = setInterval(function () {
      const now = new Date().getTime();
      const distance = targetDate - now;
      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);
      document.getElementById("countdown").innerHTML = days + "d " + hours + "h " + minutes + "m " + seconds + "s ";
      if (distance < 0) {
        clearInterval(countdownInterval);
        document.getElementById("countdown").innerHTML = "Let's Party! 🎉";
      }
    }, 1000);
  </script>
</body>
</html>

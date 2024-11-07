<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Xtrawl - The Good Looking, Rich, 6'2 Blasian</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Meet Xtrawl</h1>
  </header>

  <section id="bio">
    <img src="xtrawl-image.jpg" alt="Xtrawl" class="profile-image">
    <p class="intro">Xtrawl is the definition of good looks, style, and success. Standing tall at 6'2", this Blasian sensation is all about living the high life.</p>
    <p class="details">When it comes to fashion, charisma, and wealth, Xtrawl has it all. Let’s just say they turn heads wherever they go. 😉</p>
    
    <button onclick="showPopup()">Click for a Surprise!</button>
    <div id="popup" class="hidden">
      <div class="popup-content">
        <p>Xtrawl is better. 😎</p>
        <button onclick="closePopup()">Close</button>
      </div>
    </div>
  </section>

  <footer>
    <p>&copy; 2024 Xtrawl's Fan Club. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #000000;
  color: #333;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  overflow: hidden;
}

header {
  background-color: #3a3a3a;
  color: white;
  padding: 20px;
  width: 100%;
  text-align: center;
}

h1 {
  margin: 0;
}

#bio {
  text-align: center;
  margin-top: 30px;
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  width: 80%;
  max-width: 800px;
}

.profile-image {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin: 20px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.intro {
  font-size: 1.2em;
  margin: 10px 0;
}

.details {
  font-size: 1em;
  color: #555;
}

button {
  background-color: #ff5733;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  font-size: 1em;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #e84e2b;
}

#popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.popup-content {
  background-color: white;
  padding: 30px;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
}

.popup-content p {
  font-size: 1.5em;
  color: #ff5733;
}

#surprise {
  margin-top: 20px;
  font-size: 1.1em;
  color: #008080;
  display: none;
}

footer {
  margin-top: 30px;
  padding: 20px;
  background-color: #3a3a3a;
  color: white;
  width: 100%;
  text-align: center;
}

/* Snowfall effect */
.snow {
  position: absolute;
  top: 0;
  left: 0;
  pointer-events: none;
  z-index: 10;
  width: 100%;
  height: 100%;
  display: block;
}

.snowflake {
  position: absolute;
  top: -10px;
  width: 10px;
  height: 10px;
  background-color: red;
  border-radius: 50%;
  opacity: 0.8;
  animation: fall 3s linear infinite;
}

@keyframes fall {
  to {
    transform: translateY(100vh);
  }
}
function showPopup() {
  // Display the popup
  var popup = document.getElementById("popup");
  popup.style.display = "flex";

  // Start snow falling effect
  createSnow();
}

function closePopup() {
  // Close the popup
  var popup = document.getElementById("popup");
  popup.style.display = "none";
}

function createSnow() {
  const snowContainer = document.createElement("div");
  snowContainer.classList.add("snow");
  document.body.appendChild(snowContainer);

  // Create multiple snowflakes
  for (let i = 0; i < 100; i++) {
    const snowflake = document.createElement("div");
    snowflake.classList.add("snowflake");
    snowflake.style.left = `${Math.random() * 100}vw`;
    snowflake.style.animationDuration = `${Math.random() * 3 + 2}s`;
    snowContainer.appendChild(snowflake);
  }

  // Optional: Clean up after snowfall ends
  setTimeout(() => {
    snowContainer.remove();
  }, 5000);
}

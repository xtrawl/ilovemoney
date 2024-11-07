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
    
    <button onclick="showSecret()">Click for a Surprise!</button>
    <p id="surprise" class="hidden">Xtrawl's secret? They're the heartthrob of the coding world and already a tech billionaire at 25. 😎</p>
  </section>

  <footer>
    <p>&copy; 2024 Xtrawl's Fan Club. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
/* styles.css */

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
  color: #333;
  display: flex;
  flex-direction: column;
  align-items: center;
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

#surprise {
  margin-top: 20px;
  font-size: 1.1em;
  color: #008080;
  display: none;
}

.hidden {
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
// script.js

function showSecret() {
  var secret = document.getElementById("surprise");
  secret.style.display = "block";
}

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Minecraft Squid Game Tournament</title>
<style>
body {
margin: 0;
font-family: 'Segoe UI', sans-serif;
background-color: #111;
color: #fff;
}

header {
background: linear-gradient(to right, #e50914, #720e9e);
padding: 50px 20px;
text-align: center;
}

header h1 {
font-size: 2.5em;
margin-bottom: 10px;
}

header p {
font-size: 1.2em;
}

header .btn {
background: #fff;
color: #111;
padding: 10px 20px;
text-decoration: none;
font-weight: bold;
border-radius: 5px;
margin-top: 20px;
display: inline-block;
}

nav {
background-color: #1f1f1f;
display: flex;
justify-content: center;
padding: 10px;
}

nav a {
color: white;
text-decoration: none;
margin: 0 15px;
font-weight: bold;
}

section {
padding: 40px 20px;
max-width: 800px;
margin: auto;
}

.about ul {
list-style: none;
padding: 0;
}

.about ul li {
background: #222;
margin: 10px 0;
padding: 10px;
border-radius: 5px;
}

.register form {
display: flex;
flex-direction: column;
gap: 10px;
max-width: 400px;
margin: auto;
}

.register input, .register button {
padding: 10px;
font-size: 1em;
}

.register button {
background: #e50914;
color: #fff;
border: none;
cursor: pointer;
border-radius: 5px;
}

.rules ol {
padding-left: 20px;
}

footer {
text-align: center;
padding: 20px;
background: #222;
color: #aaa;
margin-top: 40px;
}

.timer {
font-size: 1.5em;
margin: 20px 0;
background: #222;
padding: 15px;
border-radius: 8px;
text-align: center;
}

.leaderboard table {
width: 100%;
border-collapse: collapse;
margin-top: 20px;
}

.leaderboard th, .leaderboard td {
padding: 10px;
border: 1px solid #444;
text-align: center;
}

.leaderboard th {
background-color: #e50914;
}

a {
color: #e50914;
}
</style>
</head>
<body>

<header>
<h1>🦑 Minecraft Squid Game Tournament</h1>
<p>Survive. Compete. Win Big!</p>
<p>🎮 Server IP: <strong>play.yoursquidserver.com</strong></p>
<a href="#register" class="btn">Register Now</a>
</header>

<nav>
<a href="#about">About</a>
<a href="#rules">Rules</a>
<a href="#leaderboard">Leaderboard</a>
<a href="#register">Register</a>
<a href="#contact">Contact</a>
</nav>

<section class="timer">
⏳ Event Starts In: <span id="countdown">Loading...</span>
</section>

<section class="about" id="about">
<h2>About the Tournament</h2>
<p>Join our epic Minecraft Squid Game tournament where players compete in classic Squid Game challenges inside Minecraft. Only one winner will take the grand prize!</p>
<ul>
<li>🔴 Red Light Green Light</li>
<li>🍪 Honeycomb Challenge</li>
<li>⚔️ Tug of War</li>
<li>🏃‍♂️ Glass Bridge & More</li>
</ul>
<p>📍 Server Address: <code>play.yoursquidserver.com</code></p>
<p>📢 Join our Discord: <a href="https://discord.gg/84C7KZMXdq" target="_blank">https://discord.gg/84C7KZMXdq</a></p>
</section>

<section class="rules" id="rules">
<h2>Game Rules</h2>
<ol>
<li>No hacking or cheating.</li>
<li>One Minecraft account per player.</li>
<li>Follow instructions from the Game Master.</li>
<li>Be respectful and fair to other participants.</li>
<li>Have fun and play fair!</li>
</ol>
</section>

<section class="leaderboard" id="leaderboard">
<h2>🏆 Leaderboard</h2>
<table>
<thead>
<tr>
<th>Rank</th>
<th>Player</th>
<th>Points</th>
</tr>
</thead>
<tbody>
<tr><td>1</td><td>EpicSteve</td><td>95</td></tr>
<tr><td>2</td><td>BlockMaster</td><td>88</td></tr>
<tr><td>3</td><td>RedLightPro</td><td>80</td></tr>
<!-- Add more players here -->
</tbody>
</table>
</section>

<section class="register" id="register">
<h2>Register to Participate</h2>
<form>
<input type="text" placeholder="Your Minecraft Username" required />
<input type="email" placeholder="Your Email" required />
<button type="submit">Join the Game</button>
</form>
</section>

<section id="contact">
<h2>Contact Us</h2>
<p>For any queries, reach out to us at:</p>
<p><a href="mailto:squidgame@minecraftarena.com">squidgame@minecraftarena.com</a></p>
</section>

<footer>
<p>© 2025 Minecraft Arena | All Rights Reserved</p>
</footer>

<script>
// Timer logic: Set your event date here
const eventDate = new Date("2025-07-23T18:00:00").getTime();
const countdownElement = document.getElementById("countdown");

const timer = setInterval(() => {
const now = new Date().getTime();
const diff = eventDate - now;

if (diff <= 0) {
clearInterval(timer);
countdownElement.innerText = "The event has started!";
return;
}

const days = Math.floor(diff / (1000 * 60 * 60 * 24));
const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
const seconds = Math.floor((diff % (1000 * 60)) / 1000);

countdownElement.innerText = `${days}d ${hours}h ${minutes}m ${seconds}s`;
}, 1000);

// Dummy form submission
document.querySelector("form").addEventListener("submit", function(e) {
e.preventDefault();
alert("Registration submitted! We'll contact you soon.");
});
</script>

</body>
</html>

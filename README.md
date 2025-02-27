<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Basketball Prompt App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #2c3e50; /* Dark blue background */
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
    }
    .container {
      background-color: rgba(0, 0, 0, 0.7);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
      max-width: 500px;
      width: 100%;
    }
    h1 {
      font-size: 2.5em;
      margin-bottom: 20px;
      color: #e74c3c; /* Red color for the title */
    }
    #prompt {
      font-size: 1.5em;
      margin: 20px 0;
      color: #f1c40f; /* Yellow color for the prompt */
    }
    button {
      background-color: #3498db; /* Default blue color */
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 1.2em;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button:hover {
      opacity: 0.9;
    }
    .image-container {
      margin-top: 20px;
    }
    .image-container img {
      width: 100%;
      max-width: 300px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }
  </style>
</head>
<body>
  <!-- App Content -->
  <div class="container">
    <h1>Basketball Prompt Generator</h1>
    <p>Click the button to get a random basketball prompt!</p>
    <div id="prompt">Your prompt will appear here.</div>
    <button id="generateButton" onclick="generatePrompt()">Generate Prompt</button>
    <div class="image-container">
      <img id="basketballImage" src="https://images.unsplash.com/photo-1519861531473-9200262188bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1951&q=80" alt="Basketball Image">
    </div>
  </div>

  <script>
    // List of basketball prompts
    const prompts = [
      "Describe your favorite NBA moment.",
      "Who do you think is the GOAT of basketball?",
      "Predict the next NBA champion.",
      "What's your favorite basketball drill?",
      "If you could play with any NBA player, who would it be?",
      "What's the most memorable game you've watched?",
      "How would you improve your basketball skills?",
      "What's your favorite basketball team and why?",
      "Describe your dream basketball court.",
      "What's the best basketball advice you've received?",
      "If you could invent a new basketball rule, what would it be?",
      "What's the most underrated basketball skill?",
      "Who is your favorite basketball commentator and why?",
      "What's the most iconic basketball shoe of all time?",
      "If you could coach an NBA team, which one would it be?",
      "What's the best basketball movie ever made?",
      "What's your pre-game ritual?",
      "What's the hardest part of playing basketball?",
      "If you could dunk on any player, who would it be?",
      "What's the most important quality for a basketball player?"
    ];

    // List of basketball images
    const images = [
      "https://images.unsplash.com/photo-1519861531473-9200262188bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1951&q=80",
      "https://images.unsplash.com/photo-1546519638-68e109498ffc?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80",
      "https://images.unsplash.com/photo-1600185365483-26d7a4cc7519?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80",
      "https://images.unsplash.com/photo-1600185365926-3a2ce3cdb9eb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80",
      "https://images.unsplash.com/photo-1600185365483-26d7a4cc7519?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
    ];

    // List of colors for the button
    const colors = [
      "#3498db", // Blue
      "#e74c3c", // Red
      "#2ecc71", // Green
      "#f1c40f", // Yellow
      "#9b59b6", // Purple
      "#1abc9c", // Teal
      "#e67e22", // Orange
      "#34495e"  // Dark Blue
    ];

    // Function to generate a random prompt, image, and button color
    function generatePrompt() {
      // Generate random prompt
      const randomPrompt = prompts[Math.floor(Math.random() * prompts.length)];
      document.getElementById('prompt').innerText = randomPrompt;

      // Generate random image
      const randomImage = images[Math.floor(Math.random() * images.length)];
      document.getElementById('basketballImage').src = randomImage;

      // Generate random button color
      const randomColor = colors[Math.floor(Math.random() * colors.length)];
      document.getElementById('generateButton').style.backgroundColor = randomColor;
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Random Quote Generator</title>
  <style>
    body {
      background: #34495e;
      color: #ecf0f1;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      padding: 20px;
    }

    .quote-box {
      background: #2c3e50;
      padding: 30px;
      border-radius: 10px;
      text-align: center;
      max-width: 600px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
    }

    .quote {
      font-size: 24px;
      margin-bottom: 15px;
    }

    .author {
      font-size: 18px;
      color: #bdc3c7;
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      background-color: #e67e22;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="quote-box">
    <div class="quote" id="quote">Click the button to get a quote!</div>
    <div class="author" id="author">—</div>
    <button onclick="generateQuote()">New Quote</button>
  </div>

  <script>
    const quotes = [
      { text: "The best way to get started is to quit talking and begin doing.", author: "Walt Disney" },
      { text: "Don’t let yesterday take up too much of today.", author: "Will Rogers" },
      { text: "It’s not whether you get knocked down, it’s whether you get up.", author: "Vince Lombardi" },
      { text: "If you are working on something exciting, it will keep you motivated.", author: "Steve Jobs" },
      { text: "Success is not in what you have, but who you are.", author: "Bo Bennett" },
      { text: "Act as if what you do makes a difference. It does.", author: "William James" },
      { text: "Happiness is not something ready made. It comes from your own actions.", author: "Dalai Lama" },
    ];

    function generateQuote() {
      const randomIndex = Math.floor(Math.random() * quotes.length);
      const quote = quotes[randomIndex];
      document.getElementById("quote").textContent = `"${quote.text}"`;
      document.getElementById("author").textContent = `— ${quote.author}`;
    }
  </script>
</body>
</html># Random-quote-generator-

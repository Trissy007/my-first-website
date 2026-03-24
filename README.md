├── index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Move to Kentucky</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Hello! I'm moving from Romania to Kentucky</h1>
    </header>

    <main>
        <section class="about-me">
            <p>Hi, my name is [Your Name]! I'm about to start college in Kentucky, USA. This is a big change for me, coming from Romania. I'm curious about the culture, lifestyle, and everything I should expect as I move there.</p>
        </section>

        <section class="question">
            <p>If you've ever moved to Kentucky or studied there, what advice would you give me? What should I expect living and studying in a new country?</p>
            <textarea id="userInput" placeholder="Write your advice here..."></textarea>
            <button id="submitBtn">Submit</button>
            <p id="response"></p>
        </section>
    </main>

    <footer>
        <p>Thanks for visiting my page! 😊</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
├── style.css       
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    color: #333;
    margin: 0;
    padding: 0;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
    max-width: 800px;
    margin: 0 auto;
}

textarea {
    width: 100%;
    height: 100px;
    margin-top: 10px;
    padding: 10px;
    font-size: 16px;
}

button {
    margin-top: 10px;
    padding: 10px 20px;
    font-size: 16px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

footer {
    text-align: center;
    padding: 20px;
    background-color: #ddd;
    margin-top: 40px;
}
└── script.js    
document.getElementById('submitBtn').addEventListener('click', function() {
    const input = document.getElementById('userInput').value;
    if(input.trim() === "") {
        document.getElementById('response').innerText = "Please write something first!";
    } else {
        document.getElementById('response').innerText = `Thanks for your advice: "${input}"!`;
        document.getElementById('userInput').value = "";
    }
});

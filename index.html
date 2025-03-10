<meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Esfam Benin University Chatbot</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="chatbot-container">
        <div class="chat-header">
            <img src="logo.png" alt="Esfam Benin University Logo">
            <h3>Esfam Benin University Chatbot</h3>
        </div>
        <div class="chat-body" id="chat-body">
            <div class="chat-message bot">Welcome to Esfam Benin University! How can I assist you today?</div>
        </div>
        <div class="chat-footer">
            <input type="text" id="user-input" placeholder="Type your question..." onkeypress="handleKeyPress(event)">
            <button onclick="sendMessage()">Send</button>
            <button onclick="startSpeechRecognition()">🎙️</button>
        </div>
    </div>

    <script src="script.js"></script>

</body>
</html>


<style>.chatbot-container {
    width: 350px;
    position: fixed;
    bottom: 20px;
    right: 20px;
    border-radius: 10px;
    background: white;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
    overflow: hidden;
}

.chat-header {
    background: #004080;
    color: white;
    padding: 10px;
    text-align: center;
    font-size: 16px;
}

.chat-header img {
    width: 40px;
    height: 40px;
    vertical-align: middle;
    margin-right: 10px;
}

.chat-body {
    max-height: 300px;
    overflow-y: auto;
    padding: 10px;
}

.chat-message {
    padding: 8px 12px;
    margin: 5px;
    border-radius: 5px;
    max-width: 80%;
}

.bot {
    background: #f1f1f1;
    align-self: flex-start;
}

.user {
    background: #004080;
    color: white;
    align-self: flex-end;
}

.chat-footer {
    display: flex;
    padding: 10px;
    border-top: 1px solid #ddd;
}

.chat-footer input {
    flex: 1;
    padding: 8px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.chat-footer button {
    background: #004080;
    color: white;
    border: none;
    padding: 8px 12px;
    margin-left: 5px;
    cursor: pointer;
}
</style><script>document.addEventListener("DOMContentLoaded", function () {
    document.getElementById("user-input").focus();
});

function handleKeyPress(event) {
    if (event.key === "Enter") {
        sendMessage();
    }
}

function sendMessage() {
    let userInput = document.getElementById("user-input").value.trim();
    if (userInput === "") return;

    appendMessage("user", userInput);
    document.getElementById("user-input").value = "";

    setTimeout(() => {
        getBotResponse(userInput.toLowerCase());
    }, 500);
}

function appendMessage(sender, message) {
    let chatBody = document.getElementById("chat-body");
    let messageElement = document.createElement("div");
    messageElement.classList.add("chat-message", sender);
    messageElement.innerText = message;
    chatBody.appendChild(messageElement);
    chatBody.scrollTop = chatBody.scrollHeight;

    if (sender === "bot") {
        speakResponse(message);
    }
}

function getBotResponse(userInput) {
    const responses = {
        "hello": "Hello! How can I help you today?",
        "admission requirements": "Admission requirements vary by program. Check here: [https://www.esfambeninuni.com/index.php]",
        "courses": "We offer various programs in Science, Business, and Humanities. See the list here: [https://www.esfambeninuni.com/academics.php]",
        "fees": "Tuition fees vary by course. Check here: [insert link]",
        "application": "Apply at https://www.esfambeninuni.com/applynow.php. Need help?",
        "student portal": "Access the student portal here: [https://portal.esfambeninuni.com/]",
        "contact": "Reach us via email at [info@esfambeninuni.con] or call +2348067279904.",
        "thank you": "You're welcome! Let me know if you need more help.",
        "bye": "Goodbye! Have a great day."
    };

    for (let key in responses) {
        if (userInput.includes(key)) {
            appendMessage("bot", responses[key]);
            return;
        }
    }

    // If no predefined response, use AI API
    fetchAIResponse(userInput);
}

function fetchAIResponse(query) {
    const apiKey = "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";  // Replace with actual AI API key
    fetch(`https://api.openai.com/v1/completions`, {
        method: "POST",
        headers: {
            "Content-Type": "application/json",
            "Authorization": `Bearer ${apiKey}`
        },
        body: JSON.stringify({
            model: "gpt-4",
            prompt: `User asked: ${query}. Provide a helpful answer.`,
            max_tokens: 100
        })
    })
    .then(response => response.json())
    .then(data => {
        let aiResponse = data.choices[0].text.trim();
        appendMessage("bot", aiResponse);
    })
    .catch(error => {
        console.error("Error fetching AI response:", error);
        appendMessage("bot", "I'm not sure about that. Please check the university website.");
    });
}

// Speech Recognition (Voice Input)
function startSpeechRecognition() {
    const recognition = new (window.SpeechRecognition || window.webkitSpeechRecognition)();
    recognition.lang = "en-US";
    recognition.start();

    recognition.onresult = function (event) {
        let userInput = event.results[0][0].transcript;
        document.getElementById("user-input").value = userInput;
        sendMessage();
    };

    recognition.onerror = function (event) {
        console.error("Speech recognition error:", event.error);
    };
}

// Text-to-Speech (Voice Output)
function speakResponse(text) {
    const speech = new SpeechSynthesisUtterance(text);
    speech.lang = "en-US";
    window.speechSynthesis.speak(speech);
}
</script>
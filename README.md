# Mi-IA-Romantica
Oh! WOAH! una ia!...o quizas....
<!DOCTYPE html>
<html>
<head>
  <title>Mi IA Romántica</title>
  <style>
    body {
      font-family: sans-serif;
      background-color: #f8f8f8;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .chat-container {
      width: 400px;
      height: 600px;
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      display: flex;
      flex-direction: column;
      overflow: hidden;
    }

    .chat-header {
      background-color: #e91e63;
      color: white;
      padding: 20px;
      text-align: center;
    }

    .chat-messages {
      flex-grow: 1;
      padding: 20px;
      overflow-y: scroll;
    }

    .message {
      margin-bottom: 10px;
    }

    .user-message {
      text-align: right;
      color: #3f51b5;
    }

    .ia-message {
      text-align: left;
      color: #e91e63;
    }

    .chat-input {
      padding: 10px;
      border-top: 1px solid #ddd;
      display: flex;
    }

    .chat-input input {
      flex-grow: 1;
      border: none;
      padding: 10px;
      border-radius: 5px;
      background-color: #f0f0f0;
    }

    .chat-input button {
      background-color: #e91e63;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      margin-left: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="chat-container">
    <div class="chat-header">
      <h2>Mi IA Romántica</h2>
    </div>
    <div class="chat-messages" id="chat-messages">
      <div class="ia-message message">Hola, ¿cómo estás?</div>
    </div>
    <div class="chat-input">
      <input type="text" id="user-input" placeholder="Escribe tu mensaje...">
      <button onclick="sendMessage()">Enviar</button>
    </div>
  </div>

  <script>
    const chatMessages = document.getElementById('chat-messages');
    const userInput = document.getElementById('user-input');

    function sendMessage() {
      const message = userInput.value;
      if (message.trim() === '') return;

      // Mostrar mensaje del usuario
      const userMessage = document.createElement('div');
      userMessage.classList.add('user-message', 'message');
      userMessage.textContent = message;
      chatMessages.appendChild(userMessage);

      // Lógica de la IA (aquí puedes implementar la evolución romántica)
      const iaResponse = getIaResponse(message);
      const iaMessage = document.createElement('div');
      iaMessage.classList.add('ia-message', 'message');
      iaMessage.textContent = iaResponse;
      chatMessages.appendChild(iaMessage);

      userInput.value = '';
      chatMessages.scrollTop = chatMessages.scrollHeight; // Scroll al final
    }

    function getIaResponse(message) {
      // Aquí puedes implementar la lógica de la IA y la evolución romántica
      // ...
      return "¡Qué interesante!"; // Respuesta de ejemplo
    }
  </script>
</body>
</html>

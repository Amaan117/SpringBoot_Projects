# Real-Time Chat Application  
### A modern, full-stack chat app built with Spring Boot, WebSocket (STOMP), and Bootstrap


## Features
- Real-time messaging (no page refresh needed)
- Multiple users can chat simultaneously
- Beautiful dark gradient UI with glassmorphism
- Messages aligned: **Your messages on the right**, others on the left
- Message timestamps and sender names
- Press **Enter** to send
- Connection status indicator (auto-reconnect)
- Responsive design (works on mobile & desktop)
- Powered by **WebSocket + STOMP over SockJS**

## Tech Stack

### Backend
- **Java 17+**
- **Spring Boot 3.x**
- **Spring WebSocket + STOMP**
- **SockJS** (fallback for older browsers)
- **Lombok**

### Frontend
- HTML5 + Bootstrap 5
- JavaScript (Vanilla)
- STOMP.js + SockJS client
- Font Awesome icons

## Project Structure
```
src/
├── main/
│   ├── java/com/chat/app/
│   │   ├── ChatApplication.java          (Main class)
│   │   ├── controller/ChatContoller.java
│   │   ├── model/ChatMessage.java
│   │   └── config/WebSocketConfig.java
│   └── resources/
│       └── static/chat.html                 (Frontend page)
```

## How to Run

### Prerequisites
- Java 17 or higher
- Maven

### Steps
1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/real-time-chat-app.git
   cd real-time-chat-app
   ```

2. Run the Spring Boot application
   ```bash
   ./mvnw spring-boot:run
   ```
   Or if using IDE: Run `ChatApplication.java`

3. Open your browser and go to:
   http://localhost:8080/chat

4. Open the same link in multiple tabs/windows → Start chatting!

## WebSocket Configuration
- Endpoint: `/chat`
- Subscribe: `/topic/messages`
- Send messages to: `/app/sendMessage`

## Contributing
Pull requests are welcome! For major changes, please open an issue first.

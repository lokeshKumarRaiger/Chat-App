# 💬 Spring Boot Chat App (WebSocket + MongoDB)

A real-time chat backend built with **Spring Boot**, **WebSocket (STOMP over SockJS)**, and **MongoDB**. This application allows users to create or join chat rooms and send messages in real-time. Messages are persisted in MongoDB for chat history retrieval.

---

## 🧰 Tech Stack

- **Spring Boot**
- **Spring WebSocket**
- **MongoDB**
- **Lombok**
- **SockJS + STOMP (frontend compatible)**
- **Cross-Origin Support** for React/Vite frontend (`http://localhost:5173`)

---

## 🚀 Features

- 📡 WebSocket-based real-time messaging
- 💬 Room creation and joining
- 📝 Persistent chat history stored in MongoDB
- 🔁 Message pagination (latest messages first)
- ✅ REST API support for room management and message retrieval

---

## 📂 Project Structure :

src/
├── main/java/com/substring/chat/
│ ├── controllers/
│ │ ├── ChatController.java
│ │ └── RoomController.java
│ ├── entities/
│ │ ├── Message.java
│ │ └── Room.java
│ ├── payload/
│ │ └── MessageRequest.java
│ ├── repositories/
│ │ └── RoomRepository.java
│ ├── WebSocketConfig.java
│ └── ChatAppBackendApplication.java
├── resources/
│ └── application.properties



📦 REST API Endpoints
🔹 Create Room
bash
Copy
Edit
POST /api/v1/rooms
Body (text/plain): "room-group-1"
🔹 Join Room
bash
Copy
Edit
GET /api/v1/rooms/{roomId}
🔹 Get Messages with Pagination
bash
Copy
Edit
GET /api/v1/rooms/{roomId}/messages?page=0&size=20
Returns the latest size messages of a room, supporting pagination.

⚙️ How to Run Locally
Clone the repo:

bash
Copy
Edit
git clone https://github.com/your-username/spring-chat-app.git
cd spring-chat-app
Add MongoDB URI to application.properties:

properties
Copy
Edit
spring.data.mongodb.uri=mongodb://localhost:27017/chat-app
Run the app:

bash
Copy
Edit
mvn spring-boot:run
Connect using frontend (like React or Vue) via WebSocket and REST APIs.

📸 Sample JSON (Room Entity)
json
Copy
Edit
{
  "id": "64a1e...",
  "roomId": "room-group-1",
  "messages": [
    {
      "sender": "Lokesh",
      "content": "Hey!",
      "timeStamp": "2025-06-13T12:00:00"
    }
  ]
}

📃 License
This project is open source and available under the MIT License.

yaml
Copy
Edit

---

### ✅ Next Steps

If you have:
- A frontend (React, etc.), I can help link it here.
- Deployment plans (Render, Heroku, etc.), I can add deployment steps.
- A demo gif or screenshot, we can include that too.

Let me know if you'd like the `README.md` file content in a downloadable format!

🙌 Author
Lokesh Kumar Raiger
📧 lokeshv2233@gmail.com
🔗 LinkedIn | GitHub





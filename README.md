# 🎬 AngSync Room

A real-time YouTube video synchronization app that allows multiple users to watch the same video together and enjoy the real sync.
![image](https://github.com/user-attachments/assets/d15a48d0-374a-41e2-a034-2c5a25ba4f6c)
![image](https://github.com/user-attachments/assets/5e35391b-e991-4b5b-8f91-c2f2554210ce)


## 🚀 Features
✅ Create or join a sync room with a unique **Room ID**.  
✅ Watch YouTube videos **in sync** with others.  
✅ **Play, pause, and seek** functionality is synchronized across all users in the room.  
✅ Change the **video URL dynamically**.  

## 🛠️ Technologies Used
- **Frontend**: HTML, JavaScript, TailwindCSS 🎨
- **Backend**: Node.js, Express.js 🖥️
- **WebSockets**: For real-time video synchronization 🔄
- **YouTube IFrame API**: For embedding and controlling YouTube videos 🎥

## ⚙️ Installation & Setup

### 📌 Prerequisites
- Install [Node.js](https://nodejs.org/)

### 📝 Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/angsync-room.git
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   node server.js
   ```
4. Open `http://localhost:8080/` in your browser. 🌐

## 🛠️ How It Works
### **Server-side (server.js) 🖥️**
- Uses **Express.js** to serve the `index.html` file.
- Uses **WebSockets** to establish real-time communication between users.
- Manages rooms and keeps track of video state (**play, pause, seek, and URL changes**).

### **Client-side (index.html & JavaScript) 🎭**
- Connects to the **WebSocket** server.
- Loads and controls the **YouTube video** using the **YouTube IFrame API**.
- Sends and receives **synchronization messages** (play, pause, seek, change URL) through **WebSockets**.

## 🔄 WebSocket Events
| 🎯 Event Type | 🔁 Sent By | 📌 Purpose |
|-------------|---------|---------|
| `join`       | Client  | User joins a room 👥 |
| `sync`       | Server  | Sends current video state to new users 🔄 |
| `play`       | Client  | Notifies all users to **play** video ▶️ |
| `pause`      | Client  | Notifies all users to **pause** video ⏸️ |
| `seek`       | Client  | Synchronizes video position ⏩ |
| `changeUrl`  | Client  | Updates video URL for all users 🔗 |

## 🔧 Issues & Improvements
🚨 **Sometimes pause/play actions don’t sync correctly.** Possible improvement: Implement a **timestamp-based synchronization mechanism**.  
⚡ **Enhance error handling** for WebSocket disconnections.  
🎨 **UI/UX improvements** for a better user experience.  

## 📜 License
📝 MIT License

## 👤 Author
📌 **Jivan Jamdar** 🚀

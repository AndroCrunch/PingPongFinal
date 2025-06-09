# 🏓 Ping Pong - Distributed Arcade Game  
*A decentralized Java implementation of the classic Pong game*

## 🚀 Overview

This project recreates the iconic **Pong** arcade game (1972) with a twist: it uses a **decentralized client-server architecture** built in Java. Players can host or join game sessions over a network, enabling smooth multiplayer matches without the need for centralized servers. The game was developed as part of the **02148 - Introduction to Coordination in Distributed Applications** course at DTU.

> 👥 Each match is peer-to-peer: one player hosts, the other joins  
> 🎮 Paddle movement, ball physics, and scoring are fully synchronized between players in real-time

---

## 🎮 Game Features

### ✅ Core Gameplay
- 🎯 Classic Ping Pong gameplay with paddle and ball
- 🎹 Paddle control via keyboard
- 💥 Ball speed increases after each paddle hit
- 🏁 Randomized ball direction on restart after scoring

### 🌐 Distributed Features
- 🧑‍🤝‍🧑 Client-server matchmaking (host & join system)
- 🌐 Real-time communication between host and client
- 🔁 Tuple space coordination model (JSpace or similar)
- 🔄 Dynamic server generation for simultaneous games

---

## 🧠 Architecture

### 🕹 Game Mechanics
- Game state updates (ball position, paddle movement, scoring) originate from the **host**  
- All movements and changes are communicated to the **client** using tuple spaces

### 🔗 Communication Protocol
- Custom protocol for game initiation, joining, paddle movement, and ball movement  
- **Petri Nets** used to model transitions between lobby states  
- **Concurrent Algorithm** ensures smooth coordination and avoids race conditions or deadlocks

---

## 🧪 Technical Highlights

- 🧾 **Protocols**: Custom protocol for game join, play, and synchronization  
- 🧩 **Petri Net Model**: Ensures logical coordination between two players  
- 🧵 **Concurrency Handling**: Tuple-space based coordination prevents livelocks and deadlocks  
- 🔀 **Dynamic Lobby System**: Supports multiple independent games simultaneously

---

## 🕹 How to Play

1. 👤 **Launch the application**  
2. 📝 Enter your **username**
3. 🚪 Choose to **host** or **join** a game  
   - If hosting: wait for another player to join  
   - If joining: enter host address
4. 🟩 When both players connect, the game starts automatically
5. 🔼 Use keyboard keys to move your paddle up/down  
6. 🏆 Score when the ball passes your opponent’s paddle!

---

## 🧑‍💻 Team & Contribution

| 👤 Name                      | 🎯 Contributions                              |
|-----------------------------|-----------------------------------------------|
| Timm Daniel Noel Rasmussen  | Protocol, Petri Net, Game Logic               |
| Laurits Møllemand Jensen    | Distributed Realization, Concurrency Model    |
| Andro Kranjcevic            | Game Logic, Tuple Coordination, Code Testing  |

---

## 📂 Repository Info

- 🗃 Full repository: [PingPongFinal](https://github.com/AndroCrunch/PingPongFinal)
- 📝 Full Report: Included in `02148___Ping_Pong2023.pdf`  
- 🔍 How coordination is handled: See Section 3 & 4 in report  
- 🎓 Course: **02148 - Introduction to Coordination in Distributed Applications**, DTU

---

## 🛠 Technologies Used

- 🧑‍💻 Java  
- 🧰 Tuple Space Coordination (JSpace)  
- 📈 Petri Nets & Protocol Diagrams  
- 🧵 Multi-threading & Synchronization  

---

> 🧩 Built as a distributed systems challenge project for DTU  
> 🎮 Play classic Pong — now with real-time networking and coordination!

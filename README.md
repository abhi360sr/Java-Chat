# Java-Chat
The Java chat application is a real-time communication tool leveraging Java's networking and Swing framework. It features a client-server model, enabling multiple users to interact seamlessly. The project serves as a comprehensive tutorial, guiding developers in building a functional desktop chat app, showcasing their Java and GUI development skill
Here's a detailed description for the README file of the Java Chat Application:

---

# Java Chat Application

## Overview

This Java Chat Application enables real-time messaging between multiple clients connected to a single server. The project consists of three main components:
1. **JavaServer**: The server application that manages client connections and broadcasts messages.
2. **JavaClient**: A console-based client application that connects to the server for sending and receiving messages.
3. **JavaClientGUI**: A graphical user interface (GUI) based client application that offers a user-friendly interface for chat interactions.

## Components

### 1. JavaServer

**File**: `JavaServer.java`

The server listens for incoming client connections on a specified port (default: 12345). It handles multiple client connections concurrently using threads. Messages received from one client are broadcasted to all connected clients. The server maintains a set of `PrintWriter` objects for each connected client to facilitate message broadcasting.

**Key Features**:
- Listens for client connections.
- Manages multiple client connections using threads.
- Broadcasts messages to all connected clients.
- Handles client disconnections gracefully.

### 2. JavaClient

**File**: `JavaClient.java`

This is a console-based client application that connects to the chat server. It allows users to send messages to the server and receive messages broadcasted by the server. The client reads user input from the console and sends it to the server, while concurrently reading and displaying messages from the server.

**Key Features**:
- Connects to the chat server.
- Sends user messages to the server.
- Displays messages received from the server.
- Uses a separate thread to handle incoming messages.

### 3. JavaClientGUI

**File**: `JavaClientGUI.java`

This is a GUI-based client application built using Swing. It provides a text field for users to input messages and a text area to display chat messages. The GUI updates in real-time to show messages from the server and other clients. 

**Key Features**:
- User-friendly graphical interface.
- Connects to the chat server.
- Text field for user message input.
- Text area for displaying chat messages.
- Real-time message updates using a separate thread for incoming messages.

## Setup and Usage

### Prerequisites

- Java Development Kit (JDK) installed on your system.
- Basic knowledge of Java and multithreading.

### How to Run

1. **Start the Server**:
   - Open a terminal/command prompt.
   - Navigate to the directory containing `JavaServer.java`.
   - Compile the server code:
     ```sh
     javac JavaServer.java
     ```
   - Run the server:
     ```sh
     java JavaServer
     ```

2. **Start the Console Client(s)**:
   - Open a new terminal/command prompt.
   - Navigate to the directory containing `JavaClient.java`.
   - Compile the client code:
     ```sh
     javac JavaClient.java
     ```
   - Run the client:
     ```sh
     java JavaClient
     ```
   - Follow the on-screen instructions to send messages.

3. **Start the GUI Client(s)**:
   - Open a new terminal/command prompt.
   - Navigate to the directory containing `JavaClientGUI.java`.
   - Compile the GUI client code:
     ```sh
     javac JavaClientGUI.java
     ```
   - Run the GUI client:
     ```sh
     java JavaClientGUI
     ```
   - Use the graphical interface to send and receive messages.

### Example Interaction

1. Start the server.
2. Start one or more clients (console or GUI).
3. Clients can now send messages by typing in the console or the GUI text field.
4. Messages will be broadcasted to all connected clients, and displayed in the console or GUI text area.

## License

This project is open-source and available under the MIT License.

---

By following the instructions above, you can set up and run your own Java Chat Application, allowing multiple clients to communicate in real-time through a server.

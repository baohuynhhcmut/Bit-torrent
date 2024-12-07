Project Structure
php
Copy code
/
├── main.js               # Entry point for the Electron application
├── preload.js            # Preload script for Electron
├── src/
│   └── Peer/
│       ├── Client/       # Client-side logic for handling torrent downloads, piece management, and peer communication
│       └── Server/       # Server-side logic for handling peer connections and managing the tracker
│   └── Tracker/          # Tracker server implementation
├── public/               # Static assets like CSS and JavaScript files for the frontend
├── pages/                # HTML files for different pages of the application
Installation
To set up the project, install the necessary dependencies:

sh
Copy code
npm install
Usage
Running the Application
1. Start the Tracker (Server-side)
First, start the tracker server by running the following command:

sh
Copy code
cd src/Tracker
node server.js
This will start the tracker server, which handles peer connections and manages the availability of torrent files.

2. Start the Application as Seeder (Client-side)
To start the application as a Seeder (a client that uploads or shares downloaded files with others), run the following command:

sh
Copy code
npm start
3. Start the Application as Leecher (Client-side)
To start the application as a Leecher (a client that downloads files from the network), run the following command:

sh
Copy code
npm start -- 1
Here, the 1 refers to a specific torrent file (for example, "received1"). You can replace 1 with another number depending on which file you want to download.

Features
Client-Side
Downloading Torrent Files: Users can download files using torrent links or .torrent files.
Seeding Torrent Files: Once a file is downloaded, users can seed the file back into the network for others to download.
Managing Peer Connections: The application establishes peer-to-peer connections and manages data transfers between peers.
Server-Side
Tracker Implementation: The tracker manages peer lists for torrent files and facilitates communication between peers.
Handling Peer Announcements: The server responds to peers announcing their presence and updates the peer list accordingly.
Scrape Requests: The server handles scrape requests to provide updated statistics on torrent health, peer availability, and download/upload progress.
License
© Huỳnh Gia Bảo. All rights reserved.
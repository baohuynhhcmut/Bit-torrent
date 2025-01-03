# BitTorrent Implementation

This project is an implementation of the BitTorrent protocol. It includes functionalities for both the client and server sides of the protocol, allowing for the downloading and seeding of torrent files.

## Installation
Install dependencies:
    ```sh
    npm install
    ```

## Usage

### Running the Application
First, start tracker:
```sh
cd src/Tracker
node server.js
```

To start the application with seeder role, run:
```sh
npm start
```
To start the application with leecher role, run:
```sh
npm start -- 1
```
where 1 is "received1" that contain downloaded file (you can choose other number)

### Features
#### Client-Side
- **Downloading Torrent Files**: Users can download files using torrent links or .torrent files.
- **Seeding Torrent Files**: Users can share downloaded files with others by seeding them back into the network.
- **Handling Peer Connections**: The application establishes peer connections and manages data transfer between peers.

#### Server-Side
- **Tracker Implementation**: The server ensures effective management of peer lists for torrent files.
- **Handling Peer Announcements**: The server responds to peers announcing their presence and shares relevant metadata.
- **Scrape Requests**: The server manages scrape requests to provide updated statistics on torrent health and peer availability.


© 2024 Huỳnh Gia Bảo. All rights reserved.

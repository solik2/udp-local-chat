# UDP Local Chat Room

A simple UDP-based chat room application that allows devices on the same local network to communicate. The application uses UDP broadcasting to enable seamless communication between multiple devices without the need for a central server.

## Features

- Easy to use command-line interface
- No server required - pure peer-to-peer communication
- Customizable usernames with persistence
- Timestamps for all messages
- Clean shutdown handling
- Works on any local network that allows UDP broadcast

## Requirements

- Python 3.6 or higher
- No additional dependencies required (uses only standard library)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/solik2/udp-local-chat.git
   cd udp-local-chat
   ```

2. No additional installation required! The script uses only Python standard libraries.

## Usage

1. Run the chat room:
   ```bash
   python chatroom.py
   ```

2. On first run:
   - Enter your desired username
   - Your name will be saved for future sessions

3. On subsequent runs:
   - You'll be asked if you want to use your saved username
   - Type 'y' to use the saved name or 'n' to enter a new one

4. Start chatting:
   - Type your message and press Enter to send
   - Messages from other devices will appear automatically
   - Press Ctrl+C to exit

## How it Works

The application uses UDP broadcasting to send messages to all devices on the local network:

1. Each instance binds to a specific port (12345 by default)
2. Messages are broadcast to the network using the broadcast address (255.255.255.255)
3. All instances running on the same network receive the messages
4. Messages include timestamps and sender names

## Limitations

- Only works on networks that allow UDP broadcast
- All devices must be on the same local network
- No message encryption or authentication
- Some networks (especially corporate) may block UDP broadcast traffic

## Contributing

Feel free to open issues or submit pull requests if you have suggestions for improvements!

## License

This project is open source and available under the MIT License.
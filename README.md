# Flutter Perplexity Clone

A Flutter-based clone of Perplexity AI, featuring real-time chat with AI-powered search capabilities. This application provides an intuitive interface for asking questions and receiving AI-generated responses with source citations.

## Features

- **AI-Powered Chat**: Real-time conversation with AI assistant
- **Smart Search**: WebSocket-based search functionality
- **Cross-Platform**: Works on mobile, web, and desktop platforms
- **Modern UI**: Clean, responsive design with dark theme
- **Source Citations**: View sources for AI responses
- **Real-time Communication**: WebSocket integration for live chat
- **Responsive Design**: Adaptive layout for different screen sizes

## Screenshots

*Screenshots will be added here*

## Getting Started

### Prerequisites

- Flutter SDK (^3.8.1)
- Dart SDK
- WebSocket server running on `localhost:8000`

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd flutter_perplexity
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Start the WebSocket server**
   ```bash
   # Make sure your WebSocket server is running on localhost:8000
   # The app expects a WebSocket endpoint at ws://localhost:8000/ws/chat
   ```

4. **Run the application**
   ```bash
   flutter run
   ```

## Project Structure

```
lib/
├── main.dart              # App entry point
├── pages/                 # Screen components
│   ├── home_page.dart     # Main home screen
│   └── chat_page.dart     # Chat interface
├── widgets/               # Reusable UI components
│   ├── search_section.dart
│   ├── answer_section.dart
│   ├── sources_section.dart
│   ├── side_bar.dart
│   ├── side_bar_button.dart
│   └── search_bar_button.dart
├── services/              # Business logic and API calls
│   └── chat_web_service.dart
└── theme/                 # App styling and colors
    └── colors.dart
```

## Dependencies

- **flutter**: Core Flutter framework
- **google_fonts**: Custom typography (Inter font)
- **web_socket_client**: Real-time communication
- **flutter_markdown**: Markdown rendering for responses
- **skeletonizer**: Loading animations
- **cupertino_icons**: iOS-style icons

## WebSocket API

The app communicates with a WebSocket server at `ws://localhost:8000/ws/chat`:

### Message Format
- **Send**: `{"query": "user question"}`
- **Receive**: 
  - Search results: `{"type": "search_result", ...}`
  - Content: `{"type": "content", ...}`

## Development

### Running Tests
```bash
flutter test
```

### Building for Production
```bash
# Android
flutter build apk

# iOS
flutter build ios

# Web
flutter build web

# Desktop
flutter build windows
flutter build macos
flutter build linux
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by [Perplexity AI](https://www.perplexity.ai/)
- Built with Flutter and Dart
- Uses WebSocket for real-time communication

## Support

If you encounter any issues or have questions, please open an issue on GitHub.

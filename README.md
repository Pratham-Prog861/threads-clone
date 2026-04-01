# Threads Clone - Expo React Native App

A modern social media application built with **Expo 55** and **React Native 0.83.4**, inspired by Meta's Threads. This project demonstrates a clean feed interface with posts, replies, likes, and user interactions.

![Expo](https://img.shields.io/badge/Expo-55.0.9-000000?style=for-the-badge&logo=expo)
![React Native](https://img.shields.io/badge/React_Native-0.83.4-61DAFB?style=for-the-badge&logo=react)
![React](https://img.shields.io/badge/React-19.2.0-20232A?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9.2-3178C6?style=for-the-badge&logo=typescript)

## 🚀 Features

- **Home Feed**: Scrollable feed of threads with pull-to-refresh functionality
- **Thread Details**: View individual threads with all replies
- **User Profiles**: Display user information with verification badges
- **Interactions**: Like threads and view reply counts
- **Mentions**: Tag other users in threads
- **Dark/Light Mode**: Automatic theme switching based on system preferences
- **Smooth Animations**: Lottie animations for loading states
- **Responsive Design**: Works on iOS, Android, and Web

## 🛠️ Tech Stack

### Core Technologies
- **Framework**: Expo 55 with expo-router for file-based routing
- **UI Library**: React Native 0.83.4
- **Language**: TypeScript 5.9.2
- **State Management**: React Context API
- **Navigation**: expo-router with @react-navigation/native

### Key Dependencies
- `lottie-react-native` - Smooth animations
- `@faker-js/faker` - Generate realistic mock data
- `react-native-reanimated` - Advanced animations
- `expo-font` - Custom font loading
- `expo-splash-screen` - Custom splash screen

## 📁 Project Structure

```bash
threads-clone/
├── app/                      # Expo Router pages
│   ├── (tabs)/              # Tab navigation screens
│   │   ├── _layout.tsx      # Tab layout configuration
│   │   ├── index.tsx        # Home feed screen
│   │   └── two.tsx          # Second tab screen
│   ├── thread-details.tsx   # Thread detail view
│   ├── modal.tsx            # Modal screen
│   ├── _layout.tsx          # Root layout
│   └── [...missing].tsx     # 404 handler
├── components/              # Reusable UI components
│   ├── ThreadItem.tsx       # Individual thread card
│   ├── ReplyItem.tsx        # Reply component
│   ├── Themed.tsx           # Theme-aware components
│   └── StyledText.tsx       # Styled text components
├── context/                 # React Context providers
│   └── thread-context.tsx   # Thread state management
├── types/                   # TypeScript type definitions
│   └── threads.ts           # Thread, User, Reply interfaces
├── utils/                   # Utility functions
│   ├── generate-dommy-data.ts  # Mock data generation
│   └── timeAgo.ts           # Time formatting
├── lottie-animations/       # Animation files
│   └── threads.json         # Loading animation
├── assets/                  # Static assets
│   ├── fonts/               # Custom fonts
│   └── images/              # App icons and images
└── constants/               # App constants
    └── Colors.ts            # Color schemes
```

## 🎯 Key Components

### Thread Context
Global state management for threads using React Context API. Provides thread data to all components in the tree.

```typescript
// Usage example
const threads = useContext(ThreadContext);
```

### ThreadItem Component
Displays individual threads in the feed with:
- Author information and avatar
- Thread content and images
- Like and reply counts
- Timestamp with timeAgo formatting

### Data Generation
Uses Faker.js to generate realistic mock data:
- Random users with profiles
- Thread content and images
- Replies and interactions
- Verification statuses

## 🚦 Getting Started

### Prerequisites
- Node.js 18+ installed
- Expo CLI installed globally (`npm install -g expo-cli`)
- iOS Simulator (for Mac) or Android Emulator
- Expo Go app (for physical device testing)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Pratham-Prog861/threads-clone.git
   cd threads-clone
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   bun install
   ```

3. **Start the development server**

   ```bash
   npm start
   # or
   bun start
   ```

4. **Run on your platform**

   - Press `i` for iOS simulator
   - Press `a` for Android emulator
   - Press `w` for web browser
   - Scan QR code with Expo Go app

## 📱 Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start Expo dev server with tunnel |
| `npm run android` | Run on Android device/emulator |
| `npm run ios` | Run on iOS simulator/device |
| `npm run web` | Run in web browser |

## 🎨 Customization

### Adding New Screens
Create a new `.tsx` file in the `app/` directory. Expo Router will automatically create routes based on file names.

### Modifying Theme
Edit `constants/Colors.ts` to customize the color scheme for light and dark modes.

### Adding Components
Place reusable components in the `components/` directory. Use `Themed.tsx` patterns for theme-aware styling.

## 🔧 Configuration

### TypeScript
The project uses strict TypeScript configuration with path aliases. See `tsconfig.json` for details.

### Expo Configuration
App configuration is managed in `app.json`:
- App name and slug
- Icon and splash screen images
- Platform-specific settings
- Plugin configurations

## 📝 Type Definitions

Core TypeScript interfaces defined in `types/threads.ts`:

- **Thread**: Main post structure with author, content, replies
- **Reply**: Comment/reply to a thread
- **User**: User profile with followers and verification status

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Inspired by [Meta's Threads](https://www.threads.net/)
- Built with [Expo](https://expo.dev/)
- Icons by [FontAwesome](https://fontawesome.com/)
- Mock data by [Faker.js](https://fakerjs.dev/)

---

**Made with ❤️ using Expo and React Native**

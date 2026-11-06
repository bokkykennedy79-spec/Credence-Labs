# Credence

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Expo](https://img.shields.io/badge/expo-1C1E24?style=for-the-badge&logo=expo&logoColor=#D04A37)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Soroban](https://img.shields.io/badge/Soroban-7D00FF?style=for-the-badge&logo=stellar&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)


[![Open Source](https://img.shields.io/badge/Open%20Source-Yes-green?style=flat-square)](https://opensource.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![React Native](https://img.shields.io/badge/React%20Native-0.81-61DAFB?style=flat-square&logo=react)](https://reactnative.dev/)
[![Soroban SDK](https://img.shields.io/badge/Soroban%20SDK-22.0.0-purple?style=flat-square)](https://soroban.stellar.org/)

**Decentralized Buy Now Pay Later (BNPL) protocol & cross-platform mobile application on Stellar Network**

[Features](#-features) • [Tech Stack](#-tech-stack) • [Quick Start](#-quick-start) • [Documentation](#-documentation) • [Contributing](#-contributing)

</div>

## 📖 About

Credence is an institutional-grade, decentralized Buy Now Pay Later (BNPL) ecosystem on the Stellar blockchain. Built with Soroban Rust smart contracts and a cross-platform React Native / Expo mobile application, it provides a seamless experience for users to access credit lines, manage loan repayments, earn reputation, and interact with the Stellar network.

### Key Features

- 🔐 **Wallet Integration** - Connect with Stellar wallets securely
- 💰 **Loan Management** - Apply for and manage BNPL loans
- 📊 **Reputation Dashboard** - View your on-chain credit score
- 🛍️ **Merchant Discovery** - Browse participating merchants
- 💳 **Payment Processing** - Easy loan repayments
- 🔔 **Push Notifications** - Stay updated on loan status
- 📱 **Cross-Platform** - iOS and Android support
- 🎨 **Modern UI** - Beautiful, responsive design with NativeWind

## 🛠 Tech Stack

**RN0.81 · TS5.9 · EXPO54 · RR19 · NW4 · RRN7 · RNA4**

### Core Technologies

| Category | Technology | Version |
|----------|-----------|---------|
| **Language** | TypeScript | 5.9 |
| **Framework** | React Native | 0.81.5 |
| **Platform** | Expo | 54.0 |
| **UI Library** | React | 19.1 |
| **Styling** | NativeWind (Tailwind) | latest |
| **Navigation** | React Navigation | 7.1 |
| **Animations** | Reanimated | 4.1 |

### Key Libraries

- 🎨 **NativeWind** - Tailwind CSS for React Native
- 🎭 **React Native Reanimated** - Smooth animations

## 📁 Monorepo Structure

The codebase is partitioned into two core components:

```
Credence/
├── contracts/               # Soroban smart contracts (Rust)
│   ├── adapter-trustless-contract/
│   ├── creditline-contract/
│   ├── liquidity-pool-contract/
│   ├── merchant-registry-contract/
│   ├── parameters-contract/
│   ├── reputation-contract/
│   └── tests/integration/
│
├── frontend/                # Cross-platform mobile app (React Native / Expo)
│   ├── app/                 # Expo Router routes
│   ├── components/          # Reusable UI components
│   ├── context/             # React context providers
│   ├── hooks/               # Custom React hooks
│   ├── services/            # API integration services
│   └── types/               # TypeScript definitions
│
├── Cargo.toml               # Rust workspace configuration
└── package.json             # Frontend package configuration
```

### 1. Smart Contracts (Rust)
```bash
# Check all Rust contracts
cargo check --workspace

# Build contracts to WASM
cargo build --target wasm32-unknown-unknown --release
```

### 2. Frontend (React Native / Expo)

## 🚀 Quick Start

### Prerequisites

- Node.js 18 LTS or higher
- Rust 1.75+ & Cargo
- npm or yarn
- iOS Simulator (Mac only) or Android Studio
- Expo Go app (for testing on physical devices)

### Installation
```bash
# Clone the repository
git clone https://github.com/Credence-app/Credence.git
cd Credence

# Install dependencies
npm install

# Copy environment file
cp .env.example .env

# Configure your .env file (see Configuration section)
```


### Running the Application
```bash
# Start Expo development server
npm start

# Run on iOS Simulator
npm run ios

# Run on Android Emulator
npm run android

# Run in web browser
npm run web
```

### Development with Expo Go

1. Install Expo Go on your iOS or Android device
2. Run `npm start`
3. Scan the QR code with your camera (iOS) or Expo Go app (Android)

### Building for Production
```bash
# Create native projects
npm run prebuild

# Build for iOS (requires Mac)
eas build --platform ios

# Build for Android
eas build --platform android
```

## 🧪 Testing
```bash
# Run linter
npm run lint

# Fix linting issues and format code
npm run format

# Run unit tests (when configured)
npm test

# Run E2E tests (when configured)
npm run test:e2e
```

## 🎨 Design System

The app uses a custom design system built with NativeWind (Tailwind CSS):

- **Colors** - Brand colors and semantic tokens
- **Typography** - Font scales and weights
- **Spacing** - Consistent spacing system
- **Components** - Reusable UI components
- **Icons** - Expo Vector Icons integration

## 🔗 Backend Integration

This app connects to the [TrustUp API](https://github.com/TrustUp-app/TrustUp-API) backend:

- REST API endpoints for all operations
- JWT-based authentication
- Real-time updates via webhooks
- Stellar transaction signing

## 📱 Platform Support

- ✅ **iOS** - iOS 13.4+
- ✅ **Android** - Android 6.0+ (API 23+)
- ⚠️ **Web** - Basic support (optimized for mobile)

## 🔐 Security

- **Secure Storage** - Encrypted storage for sensitive data
- **Biometric Auth** - Face ID / Touch ID / Fingerprint support
- **Key Management** - Never stores private keys
- **API Security** - JWT token management
- **SSL Pinning** - Certificate pinning for API calls

## 🚀 Performance

- **Optimized Rendering** - React Native best practices
- **Lazy Loading** - Code splitting and dynamic imports
- **Image Optimization** - Optimized asset loading
- **Smooth Animations** - Reanimated for 60fps
- **Efficient State** - Minimal re-renders

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](./docs/contributing.md) for:

- Development setup
- Code style guidelines
- Component patterns
- Pull request process

## 🐛 Troubleshooting

### Common Issues

**Metro bundler issues:**
```bash
# Clear cache
npx expo start -c
```

**iOS build issues:**
```bash
# Clean iOS build
cd ios && pod install && cd ..
```

**Android build issues:**
```bash
# Clean Android build
cd android && ./gradlew clean && cd ..
```

## 📞 Support

- 📖 [Documentation](./docs/)
- 🐛 [Issue Tracker](https://github.com/Credence-app/Credence/issues)
- 💬 [Discussions](https://github.com/Credence-app/Credence/discussions)

## 🙏 Acknowledgments

- [Stellar Development Foundation](https://www.stellar.org/) - For the blockchain platform
- [Expo](https://expo.dev/) - For the amazing development platform
- [React Native Community](https://reactnative.dev/) - For the mobile framework
- [NativeWind](https://www.nativewind.dev/) - For Tailwind CSS integration

---
<!-- LEADERBOARD_START -->
## 🏆 Top 3 Contributors

<div align="center">

<table>
<tr>

<td align="center">
  <a href="https://github.com/Yusufolosun">
    <img src="https://avatars.githubusercontent.com/u/175801072?v=4" width="100px;" style="border-radius:50%;" alt="Yusufolosun"/><br />
    <sub><b>🥇 @Yusufolosun</b></sub><br />
    <sub>8 contributions</sub>
  </a>
</td>

<td align="center">
  <a href="https://github.com/KevinMB0220">
    <img src="https://avatars.githubusercontent.com/u/130603817?v=4" width="100px;" style="border-radius:50%;" alt="KevinMB0220"/><br />
    <sub><b>🥈 @KevinMB0220</b></sub><br />
    <sub>6 contributions</sub>
  </a>
</td>

<td align="center">
  <a href="https://github.com/Benalex8797">
    <img src="https://avatars.githubusercontent.com/u/198606778?v=4" width="100px;" style="border-radius:50%;" alt="Benalex8797"/><br />
    <sub><b>🥉 @Benalex8797</b></sub><br />
    <sub>5 contributions</sub>
  </a>
</td>

</tr>
</table>
</div>

<!-- LEADERBOARD_END -->

---
<div align="center">

**Built with ❤️ for the Stellar ecosystem**

[![Stellar](https://img.shields.io/badge/Powered%20by-Stellar-7D00FF?style=flat-square)](https://www.stellar.org/)
[![Open Source](https://img.shields.io/badge/Open%20Source-Yes-green?style=flat-square)](https://opensource.org/)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](./LICENSE)

</div>


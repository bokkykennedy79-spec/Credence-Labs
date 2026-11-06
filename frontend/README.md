# Credence Mobile Application (Frontend)

Cross-platform mobile application for Buy Now Pay Later (BNPL) on the Stellar Network, built with React Native, Expo, and NativeWind.

## Structure

```text
frontend/
├── app/            # Expo Router file-based routes and layouts
├── components/     # React Native UI components (pages and shared)
├── context/        # React context providers (e.g. auth)
├── hooks/          # React hooks (loans, invest, auth, merchants, etc.)
├── lib/            # Utilities, API client, secure storage
├── services/       # API integration services
├── theme/          # UI theme definitions and colors
├── types/          # TypeScript type definitions and API DTOs
└── __tests__/      # Test suites
```

## Running the App

```bash
npm install
npm start
```

## Testing

```bash
npm test
```

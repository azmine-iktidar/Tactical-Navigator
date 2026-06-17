# Tactical Navigator

Tactical Navigator is a cross-platform mobile app built with **React Native** and **Expo** for location tracking and route navigation. It uses the device compass and GPS to display heading and position on a map, and lets users record, name, and review travelled routes.

## Tech Stack

- **Framework:** Expo 51 (Expo Router) + React Native 0.74, TypeScript
- **Navigation:** Expo Router, React Navigation (drawer + stack)
- **Maps & location:** `react-native-maps`, `expo-location`, `react-native-compass-heading`, `expo-sensors`
- **Backend / auth:** Supabase (`@supabase/supabase-js`)
- **State management:** Zustand
- **UI:** React Native Elements (`@rneui/themed`), Expo Linear Gradient, Reanimated, Gesture Handler
- **Connectivity:** NetInfo (online/offline awareness)
- **Other:** Expo Haptics, Expo Font, FlashList, `react-native-dotenv`

## Features

- Live map view with current location and compass heading
- Record, name, and manage travelled routes
- Accuracy and online/offline status indicators
- User authentication via Supabase
- Drawer navigation with a custom drawer and route list
- Haptic feedback and animated UI

## Project Structure

```
app/                # Expo Router entry and screens
components/
  Map/              # Map view, location button, tracking controls, indicators
  RouteList/        # Saved route list and items
  CustomDrawer.tsx, EditRouteModal.tsx, LoadingScreen.tsx
contexts/           # User store (Zustand)
hooks/              # useAuth, useRouteListHook
utils/              # LocationService, RouteService, netcheck, formatters
constants/          # Colors
assets/             # Compass dials, fonts, images
```

## Getting Started

Prerequisites: Node.js, the Expo tooling, and a Google Maps API key plus Supabase credentials (the app reads env vars via `react-native-dotenv`).

```bash
# install dependencies
npm install

# start the Expo dev server
npm start
```

### Available Scripts

| Script | Description |
|---|---|
| `npm start` | Start the Expo development server |
| `npm run android` | Build and run on Android (`expo run:android`) |
| `npm run ios` | Build and run on iOS (`expo run:ios`, requires macOS) |
| `npm run web` | Run in the browser (`expo start --web`) |
| `npm test` | Run Jest in watch mode |

## License

See the [LICENSE](LICENSE) file in this repository.

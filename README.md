# Mandarin Language Learning App

Features:

- 📱 Cross-platform iOS/Android app with Expo + Expo Router
- 🔐 Passwordless authentication with Supabase magic links
- 🧭 Personalized onboarding flow (level, motivation, interests)
- 📚 Structured Mandarin curriculum (12 chapters, 86 lessons)
- 🎧 Listening + speaking practice modes with progress tracking
- 🎙️ Voice recording and AI transcription for pronunciation practice
- 💬 Real-time AI roleplay conversations with scenario goals/tasks
- ✨ Custom scenario generation
- 📈 Speaking/listening stats and lesson completion tracking
- 💳 In-app paywall flow

## Setup

Follow these steps to install and set up the project.

### Clone the Repository

```bash
git clone https://github.com/Saad-Ali-Khan-007/mandarin-language-learning-app.git
cd mandarin-language-learning-app
```

### Prerequisites

- Node.js
- npm or pnpm
- Supabase CLI

Install Supabase CLI:

```bash
npm install supabase --save-dev
```

### Environment Variables

Create a `.env` file in the root:

```bash
EXPO_PUBLIC_SUPABASE_URL=your_supabase_project_url
EXPO_PUBLIC_SUPABASE_KEY=your_supabase_anon_key
```

### Supabase Setup

Login and link your project:

```bash
npx supabase login
npx supabase link --project-ref YOUR_PROJECT_REF
```

Apply database migrations:

```bash
npx supabase db push
```

Deploy Edge Functions:

```bash
npx supabase functions deploy chat-completion
npx supabase functions deploy transcribe-audio
npx supabase functions deploy scenario-generate
npx supabase functions deploy start-trial
```

Set required function secrets:

```bash
npx supabase secrets set OPENROUTER_API_KEY=your_openrouter_key
npx supabase secrets set SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
```

### Auth Redirect Setup

Add your app redirect URL in Supabase Auth URL configuration:

```bash
convo://
```

### Frontend

Install dependencies:

```bash
npm install
```

Run the app:

```bash
npm run start
```

Run on iOS simulator:

```bash
npm run ios
```

Run on Android emulator:

```bash
npm run android
```

Run lint:

```bash
npm run lint
```

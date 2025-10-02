# 🏥 Acko Telemedicine Platform - Frontend

An AI-powered telemedicine frontend built with Angular, featuring real-time video consultations, AI-assisted question generation, and comprehensive session management.

## 🚀 Features

### 🎥 Video Consultation
- **Real-time Video Calls**: High-quality WebRTC-based video communication
- **Secure Communication**: End-to-end encrypted video/audio streams
- **Screen Sharing**: Enhanced medical condition explanations
- **Picture-in-Picture**: Flexible viewing options

### 🎙️ Advanced Speech Recognition
- **Real-Time Transcription**: Live speech-to-text with Indian accent support
- **Bilingual Support**: Seamless Hindi + English language switching
- **Speaker Annotation**: Automatic Doctor/Patient identification
- **Confidence Scoring**: Real-time accuracy feedback and language detection
- **Advanced Statistics**: Duration, word count, language switches, and confidence metrics

### 🤖 AI-Powered Intelligence
- **Reflexive Question Generation**: Context-aware medical questions for insurance underwriting
- **Sentiment Analysis**: Detect patient distress, confusion, or emotional state
- **Risk Assessment**: Automatic flagging of high-risk medical indicators
- **Medical Context Extraction**: Identify symptoms, conditions, and medications
- **Question Categorization**: Binary, Scale, and Open-ended question types
- **Priority-based Display**: High, Medium, Normal priority questions

### 💬 Real-time Communication
- **Text Messaging**: Share notes and links during consultations
- **File Sharing**: Upload and share medical reports and images
- **AI-Powered Suggestions**: Context-aware responses and questions

### 🧠 Session Management
- **Multi-day Context Retention**: Maintain conversation context across sessions
- **Session History Search**: Find and load previous consultations
- **Context-aware Questions**: Generate questions based on prior session data
- **Risk Level Tracking**: Monitor patient risk across multiple consultations
- **Session Analytics**: Track consultation patterns and outcomes
- **Export Functionality**: Download sessions as JSON files

## 🛠 Tech Stack

- **Framework**: Angular 17+ (Standalone Components)
- **Language**: TypeScript 5.0+
- **Styling**: Tailwind CSS 3.4+
- **Video**: WebRTC with Simple-Peer
- **State Management**: RxJS & Angular Signals
- **HTTP Client**: Angular HttpClient
- **Routing**: Angular Router
- **Forms**: Angular Reactive Forms
- **Icons**: Lucide Angular
- **Backend**: Firebase (Authentication, Firestore, Storage)
- **AI Integration**: Google Gemini API

## 📋 Prerequisites

- Node.js 18+ and npm 9+
- Angular CLI 17+ (`npm install -g @angular/cli`)
- Modern browser with WebRTC support (Chrome, Edge recommended)
- Firebase project configuration
- Google Gemini API key

## 🚀 Getting Started

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/acko-telemedicine-frontend.git
   cd acko-telemedicine-frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   
   Create `src/environments/environment.ts`:
   ```typescript
   export const environment = {
     production: false,
     firebase: {
       apiKey: 'your-firebase-api-key',
       authDomain: 'your-project.firebaseapp.com',
       projectId: 'your-project-id',
       storageBucket: 'your-project.appspot.com',
       messagingSenderId: 'your-sender-id',
       appId: 'your-app-id'
     },
     geminiApiKey: 'your-gemini-api-key'
   };
   ```

   Create `src/environments/environment.prod.ts`:
   ```typescript
   export const environment = {
     production: true,
     firebase: {
       apiKey: 'your-firebase-api-key',
       authDomain: 'your-project.firebaseapp.com',
       projectId: 'your-project-id',
       storageBucket: 'your-project.appspot.com',
       messagingSenderId: 'your-sender-id',
       appId: 'your-app-id'
     },
     geminiApiKey: 'your-gemini-api-key'
   };
   ```

4. **Start the development server**
   ```bash
   npm start
   # or
   ng serve
   ```

5. **Open your browser**
   Navigate to `http://localhost:4200`

## 📂 Project Structure

```
src/
├── app/
│   ├── components/
│   │   ├── speech-recognition/      # Speech recognition component
│   │   ├── video-call/              # Video call component
│   │   ├── chat/                    # Chat component
│   │   ├── question-panel/          # AI questions panel
│   │   ├── session-sidebar/         # Session history sidebar
│   │   └── settings/                # Settings panel
│   │
│   ├── services/
│   │   ├── auth.service.ts          # Firebase authentication
│   │   ├── firestore.service.ts     # Firestore database operations
│   │   ├── storage.service.ts       # Firebase storage operations
│   │   ├── ai.service.ts            # Gemini AI integration
│   │   ├── speech.service.ts        # Speech recognition service
│   │   ├── webrtc.service.ts        # WebRTC video call service
│   │   └── session.service.ts       # Session management
│   │
│   ├── models/
│   │   ├── session.model.ts         # Session data models
│   │   ├── question.model.ts        # Question data models
│   │   ├── transcript.model.ts      # Transcript data models
│   │   └── user.model.ts            # User data models
│   │
│   ├── guards/
│   │   └── auth.guard.ts            # Route authentication guard
│   │
│   ├── interceptors/
│   │   └── http-error.interceptor.ts # HTTP error handling
│   │
│   ├── pipes/
│   │   ├── time-format.pipe.ts      # Time formatting
│   │   └── safe-html.pipe.ts        # Sanitize HTML
│   │
│   ├── pages/
│   │   ├── login/                   # Login page
│   │   ├── dashboard/               # Dashboard page
│   │   ├── consultation/            # Consultation page
│   │   └── history/                 # Session history page
│   │
│   ├── app.component.ts             # Root component
│   ├── app.config.ts                # App configuration
│   └── app.routes.ts                # Application routes
│
├── assets/
│   ├── images/                      # Static images
│   └── icons/                       # Custom icons
│
├── environments/
│   ├── environment.ts               # Development environment
│   └── environment.prod.ts          # Production environment
│
└── styles/
    ├── styles.css                   # Global styles
    ├── tailwind.css                 # Tailwind imports
    └── variables.css                # CSS custom properties
```

## 🔧 Development

### Available Scripts

```bash
# Start development server
npm start
ng serve

# Build for production
npm run build
ng build --configuration production

# Run unit tests
npm test
ng test

# Run e2e tests
npm run e2e
ng e2e

# Lint code
npm run lint
ng lint

# Format code
npm run format
npx prettier --write "src/**/*.{ts,html,css}"
```

### Code Generation

```bash
# Generate component
ng generate component components/component-name

# Generate service
ng generate service services/service-name

# Generate guard
ng generate guard guards/guard-name

# Generate pipe
ng generate pipe pipes/pipe-name
```

## 🎨 Styling

### Tailwind CSS Configuration

The project uses Tailwind CSS with custom configurations:

```javascript
// tailwind.config.js
module.exports = {
  content: ['./src/**/*.{html,ts}'],
  theme: {
    extend: {
      colors: {
        primary: '#4F46E5',
        secondary: '#10B981',
        accent: '#F59E0B',
        danger: '#EF4444',
        medical: {
          light: '#EEF2FF',
          dark: '#3730A3'
        }
      }
    }
  },
  plugins: []
};
```

### Custom CSS Variables

```css
:root {
  --primary-color: #4F46E5;
  --secondary-color: #10B981;
  --danger-color: #EF4444;
  --text-primary: #1F2937;
  --text-secondary: #6B7280;
  --background: #F9FAFB;
}
```

## 🔐 Authentication

The application uses Firebase Authentication with the following methods:

- Email/Password
- Google Sign-In
- Phone Authentication (optional)

### Protected Routes

```typescript
const routes: Routes = [
  { path: 'login', component: LoginComponent },
  { 
    path: 'dashboard', 
    component: DashboardComponent,
    canActivate: [AuthGuard]
  },
  { 
    path: 'consultation/:id', 
    component: ConsultationComponent,
    canActivate: [AuthGuard]
  }
];
```

## 🌐 API Integration

### Firebase Services

```typescript
// Firestore example
import { Firestore, collection, addDoc } from '@angular/fire/firestore';

async saveSession(session: Session) {
  const sessionsRef = collection(this.firestore, 'sessions');
  return await addDoc(sessionsRef, session);
}
```

### Gemini AI Integration

```typescript
// AI Service example
async generateQuestions(context: string): Promise<Question[]> {
  const response = await this.geminiService.generateContent({
    prompt: `Generate medical questions based on: ${context}`,
    context: 'medical_consultation'
  });
  return this.parseQuestions(response);
}
```

## 📱 Responsive Design

The application is fully responsive and optimized for:

- **Desktop**: 1920px and above
- **Laptop**: 1366px - 1919px
- **Tablet**: 768px - 1365px
- **Mobile**: 320px - 767px

## ♿ Accessibility

- ARIA labels for screen readers
- Keyboard navigation support
- High contrast mode
- Focus indicators
- Alt text for images

## 🧪 Testing

### Unit Testing

```bash
# Run tests
ng test

# Run tests with coverage
ng test --code-coverage
```

### E2E Testing

```bash
# Run e2e tests
ng e2e
```

## 📦 Building for Production

```bash
# Build with production configuration
npm run build

# Build with specific environment
ng build --configuration staging
```

### Build Optimization

- Ahead-of-Time (AOT) compilation
- Tree shaking
- Minification
- Code splitting
- Lazy loading modules

## 🚀 Deployment

### Firebase Hosting

```bash
# Install Firebase tools
npm install -g firebase-tools

# Login to Firebase
firebase login

# Initialize Firebase
firebase init

# Deploy
firebase deploy --only hosting
```

### Environment Variables

Set production environment variables in `src/environments/environment.prod.ts` before building.

## 🔒 Security

- **XSS Protection**: Angular's built-in sanitization
- **CSRF Protection**: HTTP interceptors
- **Authentication**: Firebase Auth tokens
- **API Security**: Environment-based API keys
- **Content Security Policy**: Configured headers

## 🌍 Browser Support

- Chrome 90+ (recommended)
- Edge 90+
- Firefox 88+
- Safari 14+

## 📊 Performance Optimization

- Lazy loading routes
- OnPush change detection
- Virtual scrolling for lists
- Image optimization
- Bundle size optimization
- Service worker caching (PWA ready)

## 🐛 Troubleshooting

### Common Issues

**Speech recognition not working:**
- Ensure microphone permissions are granted
- Use Chrome or Edge browser
- Check internet connection

**Video call not connecting:**
- Check WebRTC compatibility
- Verify firewall settings
- Ensure HTTPS connection

**Build errors:**
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

### Coding Standards

- Follow Angular Style Guide
- Use TypeScript strict mode
- Write unit tests for components
- Document complex logic
- Use meaningful variable names

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Angular Team**: Amazing framework
- **Firebase**: Backend infrastructure
- **Google Gemini**: AI capabilities
- **Tailwind CSS**: Utility-first styling
- **Lucide**: Beautiful icons

---

**Built with ❤️ for healthcare professionals**

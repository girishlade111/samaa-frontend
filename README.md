# Samaa Music Streaming App - Frontend

Welcome to **Samaa**, a modern music streaming web application built using the **MERN stack** (MongoDB, Express.js, React.js, Node.js). Samaa provides a seamless music listening experience with features like playlist management, song search, trending tracks, and personalized libraries.

![Samaa Home Screen](public/samaa_home_screen_logo.png)

## 🚀 Live Demo

- **Frontend (Vercel)**: [https://samavibes.vercel.app](https://samavibes.vercel.app)
- **Backend Repository**: [Samaa-Backend](https://github.com/manishraj27/samaa-backend)
- **Figma Prototype**: [Samaa Music Streaming Website](https://www.figma.com/community/file/1334999908821817060/samaa-music-streaming-website)

## ✨ Features

### Core Features
- **🎵 User Authentication**: Secure sign-up, login, and logout with email verification
- **🎧 Browse & Discover**: Explore trending songs, personalized feeds, and new releases
- **📝 Playlist Management**: Create, edit, and manage custom playlists
- **❤️ Favorites/Likes**: Like songs and access them instantly from your library
- **🔍 Smart Search**: Real-time search for songs, artists, and albums
- **🎨 Modern UI/UX**: Beautiful, responsive design with glassmorphism effects
- **📱 Mobile Responsive**: Optimized for all device sizes

### Technical Features
- **Audio Player**: Custom-built audio player with waveform visualization, progress circle, and playback controls
- **Firebase Integration**: Authentication and real-time database sync
- **Saavn.dev API**: Trending and feed songs sourced from [Saavn API](https://saavn.dev/)
- **Admin Dashboard**: Content management for songs and users
- **Email Verification**: Secure account verification flow
- **Protected Routes**: Role-based access control (User/Admin)

## 🛠️ Tech Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **React** | 18.2.0 | UI library |
| **React Router DOM** | 6.22.3 | Client-side routing |
| **Axios** | 1.6.8 | HTTP client |
| **MUI (Material UI)** | 5.15.15 | Component library |
| **Emotion** | 11.11.x | CSS-in-JS styling |
| **Styled Components** | 6.1.8 | Component-scoped styles |
| **Tailwind CSS** | 3.4.3 | Utility-first CSS |
| **React Icons** | 5.0.1 | Icon library |
| **Firebase** | 10.11.0 | Auth & Database |
| **Joi** | 17.12.3 | Form validation |

### Development Tools
- **React Scripts** 5.0.1 - Build tooling
- **ESLint** - Code linting
- **Jest & React Testing Library** - Testing framework

## 📁 Project Structure

```
samaa-frontend/
├── public/
│   ├── index.html
│   ├── manifest.json
│   ├── robots.txt
│   └── assets/ (images, logos, favicons)
├── src/
│   ├── components/
│   │   ├── audioPlayer/      # Custom audio player with waveforms
│   │   ├── emailVerify/      # Email verification flow
│   │   ├── fileInput/        # File upload component
│   │   ├── playlistForm/     # Create/Edit playlist forms
│   │   ├── queue/            # Playback queue management
│   │   ├── search/           # Search components
│   │   ├── sidebar/          # Navigation sidebar
│   │   ├── songCard/         # Song display cards
│   │   ├── songForm/         # Song creation/editing
│   │   ├── songItem/         # Individual song items
│   │   ├── songs/            # Song listing components
│   │   └── widgets/          # Dashboard widgets
│   ├── admin/                # Admin panel pages
│   ├── client/               # User-facing pages
│   ├── main/                 # Main layout components
│   ├── config.js             # App configuration
│   ├── firebase.js           # Firebase initialization
│   ├── App.js                # Root component
│   └── index.js              # Entry point
├── .env.example              # Environment variables template
├── package.json
└── README.md
```

## 🔧 Getting Started

### Prerequisites
- **Node.js** >= 16.x
- **npm** >= 8.x or **yarn** >= 1.22.x
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/girishlade111/samaa-frontend.git
   cd samaa-frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` and add your configuration:
   ```env
   REACT_APP_API_BASE_URL=http://localhost:5000/api
   REACT_APP_FIREBASE_API_KEY=your_firebase_api_key
   REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
   REACT_APP_FIREBASE_PROJECT_ID=your_project_id
   REACT_APP_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
   REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
   REACT_APP_FIREBASE_APP_ID=your_app_id
   REACT_APP_SAAVN_API_URL=https://saavn.dev/api
   ```

4. **Start the development server**
   ```bash
   npm start
   # or
   yarn start
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000` to view the application.

### Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Runs the app in development mode |
| `npm run build` | Builds the app for production |
| `npm test` | Launches the test runner |
| `npm run eject` | Ejects from Create React App (irreversible) |

## 🌐 Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Import the repository in [Vercel](https://vercel.com)
3. Add environment variables in Vercel dashboard
4. Deploy!

### Netlify
1. Connect your GitHub repository
2. Build command: `npm run build`
3. Publish directory: `build`
4. Add environment variables
5. Deploy

### Docker
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npx", "serve", "-s", "build"]
```

## 📸 Screenshots

| Home | Feed | Library | Player |
|------|------|---------|--------|
| ![Home](https://github.com/manishraj27/samaa-frontend/assets/77354587/fa7f45e7-5e84-4444-9375-4a6647f06d72) | ![Feed](https://github.com/manishraj27/samaa-frontend/assets/77354587/62278b85-455e-445f-bc91-40bba86320e1) | ![Library](https://github.com/manishraj27/samaa-frontend/assets/77354587/1c396c42-9844-4414-baca-fd2283b45b72) | ![Player](https://github.com/manishraj27/samaa-frontend/assets/77354587/bc322ebc-a22d-41c8-b282-1b252f715eea) |

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Ways to Contribute
- 🐛 **Report Bugs**: Open an issue with detailed reproduction steps
- 💡 **Suggest Features**: Share your ideas for new functionality
- 🔧 **Submit PRs**: Fix bugs or implement features
- 📚 **Improve Documentation**: Help make our docs better

### Development Workflow
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes
4. Run tests: `npm test`
5. Commit your changes: `git commit -m 'Add amazing feature'`
6. Push to the branch: `git push origin feature/amazing-feature`
7. Open a Pull Request

### Code Style
- Follow the existing code style
- Use ESLint: `npm run lint`
- Write meaningful commit messages
- Add tests for new features

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 👥 Authors & Acknowledgments

- **Original Author**: [Manish Raj](https://github.com/manishraj27)
- **Maintainer**: [Girish Lade](https://github.com/girishlade111)

### Special Thanks
- [Saavn.dev](https://saavn.dev/) for providing the music API
- [Firebase](https://firebase.google.com/) for backend services
- [MUI](https://mui.com/) for the component library
- All contributors who have helped improve Samaa

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/girishlade111/samaa-frontend/issues)
- **Discussions**: [GitHub Discussions](https://github.com/girishlade111/samaa-frontend/discussions)
- **Email**: girishlade111@gmail.com

---

<div align="center">
  <p><strong>Built by <a href="https://github.com/girishlade111">Girish Lade</a></strong> · <a href="https://ladestack.in">ladestack.in</a></p>
  <p>Made with ❤️ by the Samaa Team</p>
  <p>
    <a href="https://github.com/girishlade111/samaa-frontend/stargazers">
      <img src="https://img.shields.io/github/stars/girishlade111/samaa-frontend?style=social" alt="GitHub Stars">
    </a>
    <a href="https://github.com/girishlade111/samaa-frontend/forks">
      <img src="https://img.shields.io/github/forks/girishlade111/samaa-frontend?style=social" alt="GitHub Forks">
    </a>
    <a href="https://github.com/girishlade111/samaa-frontend/issues">
      <img src="https://img.shields.io/github/issues/girishlade111/samaa-frontend" alt="GitHub Issues">
    </a>
    <a href="https://github.com/girishlade111/samaa-frontend/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/girishlade111/samaa-frontend" alt="License">
    </a>
  </p>
</div>
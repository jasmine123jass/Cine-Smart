# 🎬 CineSmart - AI-Powered Movie Recommendation System

![CineSmart](https://img.shields.io/badge/CineSmart-AI%20Powered-red)
![Java](https://img.shields.io/badge/Java-Spring%20Boot-green)
![Cloud](https://img.shields.io/badge/Cloud-Ready-blue)

CineSmart is an AI-powered movie recommendation platform with cloud deployment capabilities.

---

## 🌟 Features

### AI/ML Features (Content-Based Filtering)
- **Smart Recommendations**: Uses Cosine Similarity algorithm to recommend movies
- **100+ Movie Dataset**: Large dataset with detailed movie information
- **Multi-Factor Analysis**: Considers genre, language, director, and year
- **Personalized Suggestions**: Tailored movie recommendations based on preferences

### Cloud Features
- **Docker Support**: Containerized application
- **Cloud-Ready**: Configured for Render, Railway, AWS, Azure
- **Health Checks**: Built-in health monitoring
- **Scalable Architecture**: Designed for cloud deployment

### User Features
- **Email/Password Authentication**: Secure user login and registration
- **Search**: Find movies by title, genre, language, or director
- **Watch History**: Track your viewing history
- **Responsive Design**: Works on all devices

---

## 📁 Project Structure

```
cinesmart/
├── Frontend/                    # 🌐 Frontend (HTML/CSS/JS)
│   ├── index.html              # Main page with AI badges
│   ├── style.css               # Modern dark theme styling
│   ├── script.js               # Frontend logic
│   └── static.json             # Cloud static config
│
├── backend/                     # ☕ Backend (Java Spring Boot)
│   ├── src/main/java/
│   │   └── com/cinesmart/backend/
│   │       ├── controller/
│   │       │   ├── MovieController.java       # Movie endpoints
│   │       │   ├── AuthController.java        # Auth endpoints
│   │       │   └── AIRecommendationController.java  # 🤖 AI endpoints
│   │       ├── service/
│   │       │   ├── MovieService.java          # Movie logic
│   │       │   └── AIMovieRecommendationService.java  # 🤖 AI/ML Engine
│   │       ├── model/
│   │       │   ├── Movie.java                 # Movie model
│   │       │   └── User.java                  # User model
│   │       └── repository/
│   │           └── UserRepository.java
│   ├── Dockerfile              # 🐳 Docker config
│   └── pom.xml
│
├── docker-compose.yml          # 🐳 Docker Compose
├── render.yaml                 # ☁️ Render deployment
├── railway.json                # ☁️ Railway deployment
└── README.md
```

---

## 🤖 AI/ML Components

### AIMovieRecommendationService.java
- **Location**: `backend/src/main/java/com/cinesmart/backend/service/`
- **Algorithm**: Content-Based Filtering with Cosine Similarity
- **Features Analyzed**:
  - Genre similarity (50% weight)
  - Language match (25% weight)
  - Director similarity (15% weight)
  - Year proximity (10% weight)

### AIRecommendationController.java
- **Location**: `backend/src/main/java/com/cinesmart/backend/controller/`
- **Endpoints**:
  - `/ai/recommend/{id}` - Get AI recommendations
  - `/ai/statistics` - Movie statistics
  - `/ai/genres` - Popular genres
  - `/ai/health` - AI service health check

---

## ☁️ Cloud Components

### Deployment Options

#### 1. Render.com (Recommended - Free)
```bash
# Deploy using render.yaml
# Connect GitHub repo to Render
# Automatic deployment
```

#### 2. Railway.app
```
bash
# Deploy using railway.json
# Connect GitHub repo to Railway
```

#### 3. Docker Compose (Local)
```
bash
docker-compose up -d
```

#### 4. Manual Docker
```
bash
docker build -t cinesmart-backend ./backend
docker run -p 9090:9090 cinesmart-backend
```

---

## 🚀 Quick Start

### Prerequisites
- Java 17+
- Maven 3.8+
- Node.js (optional for frontend development)

### Run Backend
```
bash
cd backend
./mvnw spring-boot:run
```

### Run Frontend
```
bash
# Open Frontend/index.html in browser
# Or use a local server
npx serve Frontend
```

### Docker Compose
```
bash
docker-compose up --build
```

---

## 📊 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/search?q={query}` | GET | Search movies |
| `/recommend/{id}` | GET | Get recommendations |
| `/top-rated` | GET | Top rated movies |
| `/recent` | GET | Recent movies |
| `/ai/recommend/{id}` | GET | 🤖 AI recommendations |
| `/ai/statistics` | GET | 🤖 Movie statistics |
| `/ai/health` | GET | 🤖 AI health check |
| `/login` | POST | User login |
| `/register` | POST | User registration |

---

## 🛠️ Tech Stack

### Frontend
- HTML5, CSS3, JavaScript
- Font Awesome Icons
- TMDB API for posters

### Backend
- Java 17
- Spring Boot 3.x
- H2 Database
- JPA/Hibernate

### AI/ML
- Content-Based Filtering
- Cosine Similarity Algorithm
- Jaccard Similarity for genres

### Cloud
- Docker
- Render.com
- Railway.app

---

## 📈 Dataset

- **100+ Movies** across multiple languages
- **Fields**: Title, Genre, Language, Year, Rating, Director, Description
- **Languages**: English, Hindi, Telugu, Tamil, Kannada, Korean
- **Genres**: Action, Drama, SciFi, Comedy, Horror, Thriller, Romance, and more

---

## 🔧 Configuration

### Cloud Properties
Location: `backend/src/main/resources/application-cloud.properties`

```
properties
ai.recommendation.enabled=true
ai.recommendation.algorithm=cosine-similarity
ai.recommendation.dataset.size=100+
```

---

## 📝 License

This project is for educational purposes.

---

## 👨‍💻 Author

CineSmart - AI-Powered Movie Recommendations

---

## 🙏 Acknowledgments

- TMDB for movie posters
- Open Source Community
- Spring Boot Framework

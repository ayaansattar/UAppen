
# UAppen 📍

**Real-time UMass Amherst events, right on your map.**

Never miss another campus event. UAppen transforms UMass's scattered event information into an interactive, location-based discovery experience.

---

## 💡 The Problem

Students at UMass miss opportunities because campus events are scattered across dozens of platforms, buried in emails, and difficult to discover based on location. We needed a single source of truth—on a map.

---

## Demo 

<p align="center">
  <a href="https://www.youtube.com/watch?v=kfmEvdylnP0">
    <img src="https://img.youtube.com/vi/kfmEvdylnP0/hqdefault.jpg" alt="Demo video">
  </a>
</p>

## 🎯 What It Does

- **Interactive Campus Map**: Visualize all UMass events with numbered location markers
- **Smart Filtering**: Browse by category—Arts & Music, Athletics, Service, Cultural, and more
- **Walking Directions**: One-tap Google Maps navigation to any event location
- **Real-Time Updates**: Events automatically refresh every 2 hours
- **Cross-Platform**: Native iOS and Android experience
- **Student-Only Access**: @umass.edu email authentication for verified student community


---



## 🛠️ Tech Stack

**Frontend**
- React Native + Expo for cross-platform mobile development
- React Context API for theme and state management
- `react-native-maps` with custom marker rendering
- Platform-specific optimizations for iOS and Android

**Backend**
- FastAPI (Python) with async endpoints
- SQLModel ORM + SQLite for event storage
- APScheduler for automated event scraping (every 2 hours)
- Custom location normalization engine with regex-based parsing

**Services**
- Supabase for authentication (email/password + email verification)
- UMass Engage API for live event data
- Google Maps for directions and geocoding

**Key Features**
- Intelligent pagination handling (50 events per request)
- HTML sanitization and timezone conversion (UTC → Eastern)
- Automatic GPS coordinate mapping for 70+ campus buildings
- Light/dark theme with platform-specific styling

---



## 🏆 Accomplishments

✅ **100% UMass student verification** via email domain restriction
✅ **300+ events scraped daily** with zero manual intervention  
✅ **Instant category filtering** with smooth map transitions   
✅ **Custom location geocoding** for campus buildings  
✅ **Platform parity** between iOS and Android  
✅ **Seamless Google Maps integration** on both platforms  
✅ **Light/dark theme** with dynamic navbar colors  

---

## 📚 What We Learned

- **Full-Stack Mobile Architecture**: Connecting React Native, FastAPI, Supabase, and Google Maps in a real-time system
- **Supabase + Expo Integration**: Email verification flows, authentication state management, and secure API patterns
- **FastAPI Best Practices**: Async endpoints, SQLModel ORM, dependency injection, and CORS configuration
- **Web Scraping at Scale**: Pagination strategies, HTML sanitization, timezone handling, and automated scheduling
- **Cross-Platform Mobile Development**: Platform-specific rendering, native module limitations, and performance optimization
- **Team Collaboration**: Cross-environment debugging, API contract design, and coordinated deployments

---

## 🚀 What's Next

🔹 **Expanded Coverage**: Include off-campus events within 15 miles  
🔹 **In-App Ticketing**: Book tickets without leaving UAppen  
🔹 **User-Generated Events**: Students can create and promote their own events  
🔹 **AI Categorization**: Auto-classify unlabeled events into predefined categories  
🔹 **Faster Sync**: Reduce update interval from 2 hours → 15 minutes  
🔹 **Event Reminders**: Push notifications 30 minutes before events start  
🔹 **Social Features**: See which friends are attending events  

---

## 📦 Installation & Setup

```bash
# Clone the repository
git clone https://github.com/chaudharycoding/UAppen.git
cd UAppen

# Install frontend dependencies
cd UAppen
npm install

# Install backend dependencies
cd ../backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Start the backend
uvicorn app.main:app --reload

# Start the mobile app (in UAppen directory)
npx expo start
```



## Contributors

- [Shehroz Asim (@Shehroz68)](https://github.com/Shehroz68) contributed to the FastAPI event pipeline, campus location parsing, and event categorization.

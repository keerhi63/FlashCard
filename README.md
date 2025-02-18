# FlashCard
The "Simple Language Learning Flashcards"  web app is designed to help users efficiently learn and retain foreign language vocabulary through an interactive and user-friendly experience. 
This application allows users to create, edit, and manage personalized flashcards or use preloaded sets that cover common words and phrases. 
It features a quiz mode that randomly tests users on their knowledge, incorporating an adaptive learning system that prioritizes words they struggle with the most.

-- Working of the Flash Learn Webpage --

The Flash Learn webpage is a multi-page interactive flashcard learning platform designed to help users learn new languages through flashcards. 
It includes authentication, flashcards with progress tracking, and user session management without relying on APIs.  

1. User Flow  
A. Authentication (Login & Signup)
1. Signup Page (/signup) 
   - New users register with username, email, and password.  
   - Password is hashed with bcrypt and stored in MongoDB.  
   - After successful signup, they are redirected to the Login Page.  

2. Login Page (/login) 
   - Users enter credentials, which are verified against the database.  
   - On successful login, a session is created using express-session.  
   - Users are redirected to the Dashboard.  

3. Logout  
   - Users can log out, which destroys their session and redirects them to /login.  

B. Dashboard (dashboard)
1. Displays progress tracking (percentage of mastered flashcards).  
2. Provides navigation to different pages:  
   - Flashcards
   - Progress
   - Settings  

C. Flashcards Page (/flashcards)
1. Preloaded Flashcards:
   - 15 English → Spanish 
   - 15 English → French  
   - 15 English → Japanese  
   - Each language has Beginner, Intermediate, and Advanced levels.  

2. Flashcard Features:
   - Users can *flip flashcards to view translations.  
   - Can navigate using Next / Previous buttons.  
   - Can filter by language and difficulty.  
   - Each flashcard has a "Mark as Mastered" button.  

3. Marking Progress: 
   - When a flashcard is marked as mastered, it updates the progress in MongoDB.  

D. Progress Page (/progress)
1. Displays *total mastered flashcards.  
2. Shows *progress bar (percentage completed).  
3. Displays a pie chart (mastered vs. remaining cards) using Chart.js.  
4. Lists mastered flashcards.  

E. Add Flashcards Page (/add-flashcard)
1. Users can add new flashcards by providing:  
   - Word  
   - Translation 
   - Language(Spanish, French, Japanese)  
   - Difficulty Level(Beginner, Intermediate, Advanced)  

2. The new flashcard is stored in MongoDB and appears in the flashcards list.  

F. Backend (Node.js + Express.Js + MongoDB)
- Uses EJS templates to render pages dynamically.  
- Session-based authentication.  
- Stores flashcards & user progress in MongoDB.  
- Routes:  
  - /signup → User registration  
  - /login → User authentication  
  - /dashboard → User progress overview  
  - /flashcards → Flashcard display & interaction  
  - /progress → User progress visualization  
  - /add-flashcard → Adding new flashcards  

G. Deployment & Hosting
- Backend hosted on Render/Vercel.  
- MongoDB Atlas for cloud database storage  
- Tailwind CSS for styling 
- Backend hosted on Render/Vercel.  
- MongoDB Atlas for cloud database storage  
- Tailwind CSS for styling  



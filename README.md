# QuickSend AI

QuickSend AI is a powerful application that helps job seekers create personalized emails and cover letters using AI technology. The application integrates with Firebase for authentication and storage, and uses advanced AI to generate professional communications.

## Features

- 🤖 AI-powered email generation
- ✍ Cover letter creation
- 📄 Resume upload and management
- 🔍 Resume search functionality
- 💰 Subscription-based pricing plans
- 🔒 Secure authentication
- 💾 Cloud storage integration

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v18 or higher)
- npm (v9 or higher)
- python 
- flask
- genai

2. Install dependencies:
bash
npm install


3. Set up Firebase:
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com)
   - Enable Authentication, Firestore, and Storage
   - Copy your Firebase configuration

4. Create environment variables:
env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
VITE_FIREBASE_APP_ID=your_app_id


5. Start the development server:
bash
npm run dev


## Project Structure


src/
├── components/     # Reusable UI components
├── hooks/         # Custom React hooks
├── lib/           # Utility functions and configurations
├── pages/         # Application pages/routes
└── main.tsx       # Application entry point


## Key Components

- AppBar: Main navigation component
- AuthLayout: Layout wrapper for authentication pages
- Button: Reusable button component
- Input: Form input component
- ResumeUpload: Resume upload handling component
- EmailTypeSelector: Email format selection component
- GeneratedEmail: Email display component

## Authentication

The application uses Firebase Authentication with email/password sign-in. Features include:
- User registration
- Login
- Password reset
- Session management

## API Integration

The application integrates with two main API endpoints:



## Development

bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint


## Contributing

1. Fork the repository
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email support@quicksend.ai or create an issue in the repository.

2. Install dependencies:
```bash
npm install




# VirtualDress

VirtualDress is a virtual fitting room application that allows users to create a 2D virtual model of themselves by uploading their face, entering their height and weight, and then overlaying recommended clothing items from our database. The project uses a Node.js/Express backend with MongoDB for data storage, a Python + OpenCV microservice for image processing, and a React frontend for a smooth user experience.

## Features

- **User Input:** Users can input their height, weight, and upload a face image.
- **Automatic Processing:** The backend calculates the BMI and selects an appropriate body silhouette. A Python + OpenCV microservice detects and crops the user's face, then overlays it on the silhouette to create a base model.
- **Clothing Recommendations:** The app fetches clothing items from MongoDB and, optionally, uses AI (Gemini or similar) to recommend outfits based on the occasion.
- **2D Virtual Fitting:** The React frontend layers the recommended clothing images on top of the base model, allowing users to preview different outfits.
- **Optional Checkout:** A "Buy" button can be added to simulate a purchase flow.

## Prerequisites

- **Node.js** (v12 or later)
- **npm** (comes with Node.js)
- **MongoDB** (running locally or via MongoDB Atlas)
- **Python** (if using the OpenCV microservice)
- (Optional) Git

## Installation

1. **Clone the Repository**

   ```bash
   git clone <repository_url>
   cd virtualdress

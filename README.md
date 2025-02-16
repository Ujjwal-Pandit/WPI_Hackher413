# Multi-Project Repository

This repository contains two distinct projects:

1. **QuickSend AI** – An AI-powered application that helps job seekers create personalized emails, cover letters, and manage resumes.
2. **VirtualDress** – A virtual fitting room application that creates a 2D model of the user and overlays recommended clothing items.

---

## Table of Contents

- [QuickSend AI](#quicksend-ai)
  - [Features](#features)
  - [Prerequisites](#prerequisites)
  - [Installation & Setup](#installation--setup)
  - [Project Structure](#project-structure)
  - [Key Components](#key-components)
  - [Authentication & API Integration](#authentication--api-integration)
  - [Development Scripts](#development-scripts)
  - [Contributing](#contributing)
  - [License & Support](#license--support)
- [VirtualDress](#virtualdress)
  - [Features](#features-1)
  - [Prerequisites](#prerequisites-1)
  - [Installation](#installation-1)
  - [Usage Overview](#usage-overview)
  - [Future Work](#future-work)

---

## QuickSend AI

QuickSend AI is a powerful application that leverages AI technology to generate professional emails and cover letters for job seekers. It integrates with Firebase for secure authentication, data storage, and resume management.

### Features

- 🤖 **AI-Powered Generation:** Create personalized emails and cover letters.
- ✍ **Cover Letter Creation**
- 📄 **Resume Upload & Management**
- 🔍 **Resume Search Functionality**
- 💰 **Subscription-Based Pricing**
- 🔒 **Secure Authentication**
- 💾 **Cloud Storage Integration**

### Prerequisites

Before you begin, ensure you have installed:

- **Node.js** (v18 or higher)
- **npm** (v9 or higher)
- **Python**
- **Flask**
- **GenAI**

### Installation & Setup

1. **Install Dependencies**

   ```bash
   npm install
   ```

2. **Set up Firebase**

   - Create a project at the [Firebase Console](https://console.firebase.google.com).
   - Enable **Authentication**, **Firestore**, and **Storage**.
   - Copy your Firebase configuration.

3. **Configure Environment Variables**

   Create an `.env` file in the project root with:

   ```env
   VITE_FIREBASE_API_KEY=your_api_key
   VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
   VITE_FIREBASE_PROJECT_ID=your_project_id
   VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
   VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
   VITE_FIREBASE_APP_ID=your_app_id
   ```

4. **Start the Development Server**

   ```bash
   npm run dev
   ```

### Project Structure

```
src/
├── components/     # Reusable UI components
├── hooks/          # Custom React hooks
├── lib/            # Utility functions and configurations
├── pages/          # Application pages/routes
└── main.tsx        # Application entry point
```

### Key Components

- **AppBar:** Main navigation component.
- **AuthLayout:** Layout wrapper for authentication pages.
- **Button:** Reusable button component.
- **Input:** Form input component.
- **ResumeUpload:** Handles resume uploads.
- **EmailTypeSelector:** Allows selection of email formats.
- **GeneratedEmail:** Displays the generated email content.

### Authentication & API Integration

- **Firebase Authentication:** Supports email/password sign-in, registration, login, password reset, and session management.
- **API Endpoints:** The app integrates with various APIs for resume and AI-based email generation (details can be expanded as needed).

### Development Scripts

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint
```

### Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request.

### License & Support

- **License:** [MIT License](LICENSE)
- **Support:** For support, email [support@quicksend.ai](mailto:support@quicksend.ai) or open an issue in the repository.

---

## VirtualDress

VirtualDress is a virtual fitting room application that allows users to create a 2D virtual model by uploading a face image and entering personal measurements. The app processes the image using a Python + OpenCV microservice and recommends clothing items based on user input and AI analysis.

### Features

- **User Input:** Height, weight, and face image upload.
- **Automatic Processing:** Calculates BMI, selects a body silhouette, and uses a Python + OpenCV microservice to process the face image.
- **Clothing Recommendations:** Fetches items from MongoDB and optionally uses AI (e.g., Gemini) for outfit suggestions.
- **2D Virtual Fitting:** React frontend overlays clothing images on the base model.
- **Optional Checkout:** "Buy" button to simulate a purchase flow.

### Prerequisites

- **Node.js** (v12 or later)
- **npm** (comes with Node.js)
- **MongoDB** (local instance or MongoDB Atlas)
- **Python** (for the OpenCV microservice)
- *(Optional)* **Git**

### Installation

1. **Clone the Repository**

   ```bash
   git clone <repository_url>
   cd virtualdress
   ```

2. **Install Node Dependencies**

   ```bash
   npm install
   ```

3. **Configure the Backend**

   Set up your MongoDB connection and other backend configurations as required (refer to the backend documentation).

4. **Set Up the Python Microservice**

   Ensure you have Python and OpenCV installed. Follow the microservice-specific instructions (usually provided in a separate README or documentation).

### Usage Overview

- **Input Data:** Users enter their height, weight, and upload a face image.
- **Image Processing:** The Python microservice processes the image to crop the face and overlay it onto a recommended silhouette.
- **Outfit Recommendation:** The backend retrieves clothing recommendations from MongoDB (and may use AI for suggestions).
- **Virtual Fitting:** The React frontend displays the assembled 2D model with recommended outfits.
- **Checkout (Optional):** Users can simulate a purchase flow via the "Buy" button.

### Future Work

- **Enhanced AI Integration:** Improve outfit recommendations with advanced AI.
- **User Customization:** Allow users to adjust body measurements and clothing fits.
- **Payment Integration:** Implement a full checkout process for purchasing items.

---

Feel free to explore, contribute, and open issues for improvements or suggestions for either project. Happy coding!

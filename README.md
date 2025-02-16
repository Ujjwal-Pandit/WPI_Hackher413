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

# Expense Tracker Web App

This repository contains the source code for an Expense Tracker web app, built using Firebase to manage and track personal expenses effectively. The app allows users to add, view, and categorize expenses, helping them keep their finances in check.

## Features

- **User Authentication**: Secure login and signup using Firebase Authentication.
- **Expense Management**: Add, view, and categorize expenses (e.g., food, travel, utilities).
- **Real-time Data Sync**: Uses Firebase Firestore to store and retrieve expenses in real-time.
- **Responsive Design**: Accessible on both desktop and mobile devices.
- **Cloud Storage**: Upload receipts and other documents for reference using Firebase Storage.
- **Analytics**: Integrated with Firebase Analytics to track user engagement and app performance.

## Getting Started

Follow the steps below to get the app up and running on your local machine.

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine.
- A Firebase account and project set up. Follow the [Firebase Setup Documentation](https://firebase.google.com/docs/web/setup) if you don't already have one.

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/GoodnessJames/expense-tracker
    cd expense-tracker
    ```

2. **Install dependencies**:

    Inside the main project directory (`expense-tracker`), run:

    ```bash
    npm install
    ```

3. **Firebase configuration**:

    - In the `firebase/firebase.js` file, locate the `firebaseConfig` object.
    - Replace the placeholder values with your actual Firebase project configuration, which you can find in your Firebase Console (Settings > Project Settings > General > Firebase SDK snippet).
  
    ```js
    const firebaseConfig = {
      apiKey: "YOUR_API_KEY",
      authDomain: "YOUR_AUTH_DOMAIN",
      projectId: "YOUR_PROJECT_ID",
      storageBucket: "YOUR_STORAGE_BUCKET",
      messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
      appId: "YOUR_APP_ID"
    };
    ```

    - In `firebase/storage.js`, find the `BUCKET_URL` variable and set it to the `storageBucket` value from the Firebase config.

    ```js
    const BUCKET_URL = "YOUR_STORAGE_BUCKET";
    ```

4. **Run the app**:

    Start the development server by running:

    ```bash
    npm start
    ```

    The app should now be accessible at `http://localhost:3000`.

### Firebase Functions (Optional)

If your app uses Firebase Functions for backend logic (e.g., automated calculations, notifications), follow these steps:

1. Navigate to the `functions` directory:

    ```bash
    cd functions
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Deploy Firebase Functions:

    ```bash
    firebase deploy --only functions
    ```

## Project Structure

- **public/**: Contains the static assets and HTML files for the web app.
- **src/**: Contains the main source code, including components, services, and styles.
- **firebase/**: Contains Firebase configuration files and helper modules for Firebase services (e.g., authentication, Firestore, storage).
- **functions/**: Optional directory for backend Firebase Functions.

## Firebase Services Used

- **Firebase Authentication**: For user signups and logins.
- **Firestore**: Used as a real-time database to store and retrieve user expenses.
- **Firebase Storage**: For uploading and storing files (e.g., expense receipts).
- **Firebase Hosting**: To deploy the web app.
- **Firebase Functions** (optional): Backend logic for advanced features.
- **Firebase Analytics**: To track user interaction and improve app performance.

## Contribution

Feel free to open an issue if you encounter any bugs or have feature requests. Contributions via pull requests are also welcome!

### Steps to Contribute:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch-name`.
3. Make your changes and commit them: `git commit -m "Add some feature"`.
4. Push to the branch: `git push origin feature-branch-name`.
5. Open a pull request.

## License

This project is licensed under the [Apache License, version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

## Acknowledgments

This project draws inspiration from Firebase tutorials and the Firebase YouTube channel. Special thanks to the open-source community for their contributions to Firebase development.
# AI Rock Paper Scissors (Hand Tracking)

A browser-based Rock Paper Scissors game that uses your webcam and computer vision to track your hand gestures in real-time. Play against an AI opponent without touching the keyboard!

## 🎮 How to Play

1.  **Open the Game**: Double-click the `index.html` file to open it in a modern web browser (Google Chrome, Edge, or Firefox are recommended).
2.  **Allow Camera Access**: When prompted by the browser, allow access to your webcam. This is required for the hand tracking to work.
3.  **Wait for Load**: Wait a moment for the "Loading AI..." status to change to "Ready to Play!".
4.  **Start**: Click the **Start Game** button.
5.  **Make Your Move**:
    *   A 3-second countdown will appear on your video feed.
    *   Hold your hand up to the camera.
    *   Form one of the following shapes before the countdown hits 0:
        *   ✊ **Rock**: Make a fist.
        *   ✋ **Paper**: Open your hand with all fingers extended.
        *   ✌️ **Scissors**: Extend only your index and middle fingers.
6.  **Result**: The AI will reveal its move, and the winner will be announced instantly.

## 🧠 How It Works

This game runs entirely in your browser using JavaScript and HTML5. It utilizes **MediaPipe Hands**, a machine learning solution from Google, to perform hand tracking.

1.  **Video Capture**: The game accesses your webcam feed via the browser's `getUserMedia` API.
2.  **Hand Tracking**: MediaPipe analyzes each video frame to detect 21 3D landmarks on your hand (knuckles, finger tips, wrist).
3.  **Gesture Recognition**: The game logic calculates the position of your finger tips relative to your finger joints to determine if a finger is "open" or "closed".
    *   *Rock*: All fingers closed.
    *   *Paper*: All fingers open.
    *   *Scissors*: Index and Middle fingers open, others closed.
4.  **Game Logic**: Once the countdown finishes, the detected gesture is compared against a randomly generated move from the AI to determine the winner based on standard Rock Paper Scissors rules.

## 🛠 Technologies Used

*   **HTML5/CSS3**: For the user interface and layout.
*   **JavaScript**: Game logic and DOM manipulation.
*   **MediaPipe Hands**: For real-time hand detection and landmark tracking.
*   **Canvas API**: To draw the skeleton overlay on the video feed.

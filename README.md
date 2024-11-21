**AI Mouse Using Custom Hand Tracking Module**
This project implements an AI-driven Mouse Control System that uses real-time hand tracking for cursor movement and gesture-based commands. With a custom-built hand tracking module, this innovative solution provides a hands-free, gesture-controlled interface, offering an accessible and futuristic way to interact with computers.

**Key Features:**

1)Real-Time Hand Tracking:

Uses a custom hand tracking module built with MediaPipe and OpenCV.
Detects and tracks hand landmarks with high accuracy.

2) Mouse Cursor Control:

Maps hand movements to cursor movements on the screen.
Dynamically adjusts for screen resolution and camera input.

3) Gesture-Based Actions:

Clicking: Simulates mouse clicks (left or right) using gestures such as pinching fingers or specific finger movements.
Scrolling: Implements scrolling gestures by detecting changes in finger positions.
Drag and Drop: Tracks hand movements while maintaining a specific gesture to simulate drag-and-drop actions.

4) Customizable Gestures:

Custom gestures can be defined by leveraging the tracked hand landmark data and distances between points.
Smooth and Responsive:

Ensures low latency for seamless cursor movement and interaction.
Displays frames per second (FPS) for performance feedback.

**How It Works:**

Hand Tracking Module:

A class-based structure provides modular functionality for hand detection (findHands), landmark position retrieval (findPosition), and gesture recognition (fingersUp).
Key points such as fingertips and joints are identified for gesture control.

Cursor Mapping:

Hand coordinates are translated to screen coordinates using scaling factors derived from camera and display resolutions.

Gesture Actions:

Pinch Detection: Measures the distance between the thumb and index finger to trigger click actions.
Finger Movements: Detects which fingers are raised to identify gestures for scrolling or dragging.

Interaction Flow:

Captures video feed using OpenCV.
Processes each frame to detect the hand and recognize gestures.
Maps recognized gestures to predefined mouse actions.

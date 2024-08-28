+++
title = 'Tetris Game with Hand Gesture Control '    
date = 2024-04-26T01:29:35+05:30
draft = false   
tags = ["Machine Learning", "Gesture based recognition"]
+++ 
---

## About the Project
This project implements a Tetris game using Python with the added functionality of controlling the game using hand gestures detected from a webcam feed. The game utilizes the `pygame` library for graphics, `cv2` for webcam access, and `mediapipe` for hand gesture detection. Players can control the movement of Tetris pieces by gesturing left, right, rotate, and fast-drop.

## Control Flow
1. Display the webcam feed using OpenCV.
2. Dynamically adjust the fall speed of Tetris pieces based on gameplay time.
3. Detect hand gestures using `mediapipe` and process them to control Tetris piece movement.
4. Update the game state based on player actions and redraw the game window using `pygame`.
5. Continue looping until the game ends.

## Demo
![Tetris Demo](https://github.com/pritpalcodes/tetris_using_opencv/assets/90276050/e0975bc0-a96c-45bc-8603-b9a25fd69f48)

## Setting it Up
1. Clone the repository to your local machine.
2. Ensure you have Python installed along with the required libraries (`pygame`, `cv2`, `mediapipe`).
3. Run the `main.py` script to start the game.

## Results
The Tetris game with hand gesture control provides an interactive and engaging gaming experience. Players can enjoy the classic Tetris gameplay while using intuitive hand gestures to control the game, adding a new level of immersion to the gameplay.

## Literature and References
- Pygame documentation: [https://www.pygame.org/docs/](https://www.pygame.org/docs/)
- OpenCV documentation: [https://docs.opencv.org/](https://docs.opencv.org/)
- Mediapipe documentation: [https://google.github.io/mediapipe/](https://google.github.io/mediapipe/)
- Tetris gameplay mechanics: [https://tetris.fandom.com/wiki/Tetris_Guideline](https://tetris.fandom.com/wiki/Tetris_Guideline)
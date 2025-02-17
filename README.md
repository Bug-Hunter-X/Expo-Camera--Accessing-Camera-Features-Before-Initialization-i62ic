# Expo Camera Initialization Error

This repository demonstrates a common error when working with the Expo Camera API: attempting to access camera features before the camera has fully initialized.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

Accessing properties or methods of the camera object (`cameraRef.current`) before the `onCameraReady` callback has been triggered leads to undefined behavior, often resulting in crashes or errors.  This is because the camera object isn't fully initialized until Expo's internal camera setup is complete.

## Solution

Ensure that you only access camera features *after* the `onCameraReady` callback has been invoked. This ensures that the camera is ready for use, preventing errors and ensuring predictable functionality.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the error in the console (in `bug.js`).
5. Switch to `bugSolution.js` to see the corrected version.
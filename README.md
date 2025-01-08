# Firebase onAuthStateChanged Unsubscribe Issue

This repository demonstrates a common issue with Firebase's `onAuthStateChanged` listener: improper unsubscription leading to memory leaks.  The provided code showcases the problem and its solution.

## Problem

The `onAuthStateChanged` listener, while incredibly useful, requires careful handling to prevent memory leaks.  If the listener isn't unsubscribed from when it's no longer needed (e.g., when a component unmounts in React), it continues to run, potentially causing performance issues and unexpected behavior.

## Solution

The solution involves returning an unsubscription function from the component or function where the listener is initiated.  This function, when called, cleanly removes the listener, preventing further execution.

## Usage

1. Clone this repository.
2. Install Firebase (refer to Firebase documentation).
3. Configure your Firebase project.
4. Run the code (adjust to your project's setup).
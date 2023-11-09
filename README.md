# Multilingual Speech to Text

Experience the power of web-based multilingual speech-to-text conversion with this application. Powered by the Web Speech API, it allows you to transcribe spoken words into written text in real-time. Choose your preferred language and dialect for speech recognition, and enjoy the convenience of starting, stopping, and copying the transcribed text.

## Project Link

You can access the Multilingual Speech to Text application online at [Speech to Text](https://speechtotext5945.netlify.app/).

## Project Overview

This represents a web-based speech recognition application that uses the Web Speech API to transcribe spoken words into written text. The application provides real-time transcription and provides user-friendly messages to guide user interactions. It includes settings to select the language and dialect for speech recognition and features to start, stop, and copy the transcribed text.

## Code Structure

The code is structured around an object of messages that are used to display information to the user based on various conditions. These conditions include whether the speech recognition has started, whether the microphone settings are configured correctly, whether the microphone is detected, and so forth. The code includes multiple function definitions and event listeners for various user interactions, including changes in language selection, starting the speech recognition, and copying the transcribed text.

## Key Components and Functions

The key components and functions of the code can be summarized as follows:

1. `messages`: An object storing different messages to be displayed to the user under various conditions, along with the associated CSS class for styling the message.

2. Variables like `final_transcript`, `recognizing`, `onend_error`, `start_timestamp`, `recognition`, `select_language`, `select_dialect`, `final_span`, and `interim_span` are used to store data and DOM elements to be used throughout the script.

3. Event listener for "DOMContentLoaded": Initializes the application once the page has fully loaded. It populates the language options, checks browser support for `webkitSpeechRecognition`, and sets up the recognition object if supported.

4. Functions like `recognition.onstart`, `recognition.onerror`, `recognition.onend`, and `recognition.onresult` define the behavior of the speech recognition service during different stages of its operation.

5. `updateCountry()`: A function that updates the dialect options based on the selected language.

6. Event listeners for "change" on `#select_language`, "click" on `#start_button`, and `#copy_button` define what happens when the user changes the language selection, starts or stops the speech recognition, and copies the transcribed text.

7. `copyToClipboard(text)`: A function that copies the specified text to the clipboard.

8. `showInfo(s)`: A function that updates the displayed message based on the provided key.

## Functionality

- The script first checks for browser support for `webkitSpeechRecognition`. If it is not supported, it displays a message to the user to upgrade their browser. If it is supported, it initializes the speech recognition object and sets its properties.

- The user can select a language and a dialect. Based on these selections, the `recognition.lang` property is set, which influences how the speech is transcribed.

- The user can then start the speech recognition by clicking a start button. While the recognition is active, the user's speech is transcribed in real-time and displayed to the user.

- The user can stop the recognition, and the transcribed text will be finalized.

- The user can also copy the transcribed text to the clipboard with a click of a button.

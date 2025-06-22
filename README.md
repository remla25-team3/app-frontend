#  Frontend for Restaurant Sentiment Analysis 🍽️

This repository contains the user-facing frontend for the REMLA Restaurant Sentiment Analysis application. It provides a clean, modern, and responsive user interface for users to submit restaurant reviews, receive sentiment predictions from the machine learning model, and provide feedback on the accuracy of those predictions.

The application is built as a single-page interface using vanilla HTML, CSS, and JavaScript, and is served as a static asset by a lightweight Nginx web server.

<div align="center">
  <img src="/readme-images/screen-ui.png" alt="ui-image" width="400"/>
</div>

---

### 🚀 Features

-   **Interactive text input**: A user-friendly text area for entering restaurant reviews.
-   **Real-time sentiment prediction**: Submits reviews to the backend and displays the model's sentiment prediction (Positive/Negative) along with a confidence score.
-   **User feedback loop**: Allows users to confirm or correct the model's prediction, providing valuable data for monitoring and future model retraining.
-   **Dynamic version display**: Fetches and displays the current versions of all backend components (`app-service`, `lib-version`, `model-service`) on page load.
-   **Responsive design**: The UI is designed to work well on both desktop and mobile devices.

---

### 🏛️ Architecture & Communication

This frontend is designed as a pure client-side application and acts as the presentation layer in our architecture. It communicates exclusively with the `app-service` via REST API calls.

-   **API Endpoint**: All API calls (`/predict`, `/update-prediction`, `/version`) are made to a single backend gateway, the `app-service`.
-   **Decoupling**: The frontend has no knowledge of the `model-service` or any other internal components. This separation of concerns is a key design principle.

---

### 💻 Technology Stack

-   **HTML5**: For the structure and content of the application.
-   **CSS3**: For all styling, following a modern, clean aesthetic.
-   **Vanilla JavaScript**: For all client-side logic, including API calls (using `fetch`) and dynamic DOM manipulation.
-   **Nginx**: The `Dockerfile` in this repository uses a lightweight Nginx image to serve the `index.html` file as a static asset.

---

> *Note: The visual design and CSS for the user interface were developed with assistance from Google's Gemini.*

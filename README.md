
# Exam Portal System

The **Exam Portal System** is a lightweight, web-based application designed to facilitate online examinations while also detecting potential cheating by analyzing answer similarities. Built using HTML, CSS, and JavaScript, this system provides an intuitive user interface for registration, login, answer submission, and real-time analysis of exam responses.

## Features

- **User Management**
  - **Register:** New users can sign up by providing a username and password.
  - **Login:** Registered users can log in to access the exam portal.
  
- **Answer Submission**
  - **Dynamic Answer Fields:** Users can add multiple answers on-the-fly.
  - **Submission Handling:** Answers are processed and stored along with submission time.

- **Cheating Detection**
  - **Similarity Analysis:** The system employs techniques like Jaccard similarity and sequence matching to compare submitted answers.
  - **Disjoint Set Union (DSU):** Uses DSU (Union-Find) algorithm to group users with suspiciously similar submissions.
  - **Detailed Debug Output:** Provides a breakdown of similarities (common and differing significant words) and displays a similarity matrix for all submissions.

- **Test Data Generation**
  - Easily add test data to simulate multiple user interactions and view how the system detects potential cheating.

## How It Works

1. **User Interaction:**  
   Users interact with the portal through a simple web interface that includes separate sections for registration, login, answer submission, and cheating detection.

2. **Answer Processing:**  
   Submitted answers are preprocessed (trimming, lowercasing, removing punctuation) and then analyzed. Significant words are extracted (excluding common words) to calculate similarity ratios between different submissions.

3. **Cheating Detection Algorithm:**  
   The system calculates similarity using a weighted combination of Jaccard similarity and sequence similarity. If the similarity between any two users’ answers exceeds the predefined threshold, those users are grouped into a cluster indicating potential cheating.

4. **Visualization:**  
   Detailed debugging information including a similarity matrix and clustered groups is output to help administrators easily identify suspicious patterns.

## Usage

1. **Open the Application:**  
   Simply open the `index.html` file in a modern web browser.

2. **Register and Login:**  
   - Register new users by entering a username and password.
   - Log in with registered credentials.

3. **Submit Answers:**  
   - Enter your username.
   - Provide answers (you can add multiple answer fields).
   - Click the "Submit Answers" button.

4. **Detect Cheating:**  
   Click the "Analyze Submissions" button to view the analysis output detailing similar submissions and potential cheating clusters.

5. **Add Test Data:**  
   Use the "Add Test Data" button (fixed at the bottom-right) to populate the system with sample data for quick testing.

## Code Structure

- **HTML:** Defines the structure of the portal with separate sections for registration, login, answer submission, and cheating detection.
- **CSS:** Provides responsive styling, ensuring a clean and user-friendly interface.
- **JavaScript:**  
  - **ExamPortal Class:** Handles user registration, login, answer submission, and cheating detection.
  - **DSU Class:** Implements the Disjoint Set Union (Union-Find) algorithm for clustering similar submissions.
  - **Utility Functions:** Functions for adding test data, handling UI interactions, and logging output.

## Prerequisites

- A modern web browser that supports HTML5, CSS3, and ES6 JavaScript.

---

Feel free to modify this README to better suit your project's specifics or to add any additional information. Enjoy building and enhancing your exam portal system!

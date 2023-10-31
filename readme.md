# PDF Editor Web Application

This is a web application for uploading, editing, and viewing PDF files. It consists of both frontend and backend components. The frontend is built using React, and the backend is implemented with Node.js using Express. This README will provide an overview of the project's structure and functionality.

[![Video Title](https://img.youtube.com/vi/dOXH4g5Qkis/0.jpg)](https://www.youtube.com/watch?v=dOXH4g5Qkis)

## Frontend

The frontend code is located in the `frontend` directory. It includes two main components:

### `main.js`
![Main Page](https://i.imgur.com/EeClENI.png)
- This component allows users to upload PDF files.
- It uses React and Axios for making HTTP requests.
- The selected file is sent to the backend for processing.
- A loading indicator is displayed while the upload is in progress.

### `page.js`
![Main Page](https://i.imgur.com/DMzCndb.png)
![Main Page](https://i.imgur.com/SFWLr5D.png)
- This component displays the uploaded PDF pages.
- Users can select pages for editing and then download the modified PDF.
- It uses React Router for navigation and Axios for making requests to the backend.
- It also displays a loading indicator while fetching and processing PDF pages.

## Backend

The backend code is located in the `backend` directory. It includes an Express.js application and handles the following functionality:
It is deployed on render so the backend shuts down while inactive.
backend api : https://pdf-editor-backend-kaj5.onrender.com/

### Uploading PDF Files

- Users can upload PDF files, which are saved and associated with a unique ID.
- The backend checks if a PDF with the same content already exists in the database.

### Fetching PDF Pages

- Users can view the uploaded PDF's pages.
- The backend converts the PDF pages to base64 format and sends them to the frontend.
- It also retrieves information about the number of pages in the PDF.

### Editing PDF Pages

- Users can select specific pages for editing and then download the modified PDF.
- The backend receives the selected pages, processes the PDF, and sends the modified PDF back to the frontend.
- The result wil be produced in the order the PDF pages were selected.

## Prerequisites

- Node.js and npm must be installed to run the project.
- You may need to install required dependencies for both the frontend and backend using `npm install`.

## How to Run

1. Clone the repository.
2. Navigate to the `frontend` and `backend` directories separately and run `npm install` to install dependencies.
3. Start the frontend and backend servers by running `npm start` in their respective directories.

## API Endpoints

- `/pdf`: POST - Upload a PDF file.
- `/pdf/:id`: GET - Retrieve the PDF pages associated with the given ID.
- `/edit/:id`: POST - Edit selected pages of a PDF with the given ID.

## Contributors

- [kamalakanta mahapatra](https://github.com/Kamalakanta01)

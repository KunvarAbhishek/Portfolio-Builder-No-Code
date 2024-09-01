# Portfolio Builder with No-Code

This project is a **No-Code Portfolio Builder** designed to help users create professional portfolios and resumes effortlessly, without any prior coding experience. The application is built with **Node.js, MongoDB, HTML, CSS, and JavaScript** and allows users to choose from six different pre-designed templates, customize their details, and instantly download the portfolio or resume in a zip file format. It also offers a resume-building feature that downloads resumes in PDF format.

## Table of Contents

- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [Database Details](#database-details)



## Features

1. **Signup**
   - Users can sign up by providing their full name, email, password, and phone number.
   - Credentials are securely stored in the `user` collection in MongoDB's `portfolio_builder` database.

   ![Signup Screenshot](https://github.com/user-attachments/assets/6eb757e6-aac7-4b7b-b934-9024a2fc126e)


2. **Login**
   - Users can log in using their email and password. There are also options to reset passwords.
   - Third-party login options are available (Google, Facebook, GitHub, LinkedIn).

   ![Login Screenshot](https://github.com/user-attachments/assets/91e22cca-028f-4b9b-84a5-9ceee66ef64d)


3. **Home Page**
   - The home page has a sidebar with options like Home, Build Resume, History, Contact Us, and Logout.
   - Users can select from six pre-designed templates for their portfolio without any coding. The design templates can be applied by clicking the "Use Template" button.

   ![Home Page Screenshot](https://github.com/user-attachments/assets/e58a83f2-0be9-4415-a3f0-1e890c87cc26)


4. **Build Portfolio**
   - Users fill in personal details like name, email, city, education, skills, work experience, and links (GitHub, LinkedIn).
   - The portfolio is generated based on the selected template, and the files (HTML, CSS, JS) are downloaded in a zip file for easy hosting.
   
   ![Template Selection Screenshot](https://github.com/user-attachments/assets/588d06d2-ffa7-404a-a475-0c1e66ab3ab5)

   ![Template Preview Screenshot](https://github.com/user-attachments/assets/9324f4d7-da65-49e1-897a-de0b22395437)
   
   ![Portfolio Builder Screenshot](https://github.com/user-attachments/assets/ffc0d3e0-8514-493b-a774-fa5de1f34f3c)


5. **Build Resume**
   - Similar to the portfolio, users can fill in their details, and a resume is generated as a PDF file, ready to download.

   ![Build Resume Screenshot](https://github.com/user-attachments/assets/36451ba8-0a10-4e59-adbe-1d406053e4fa)
   
   ![Resume Screenshot](https://github.com/user-attachments/assets/b875ca1b-1cbb-4a5b-bb2b-c62223074d57)
   
   ![Resume PDF Screenshot](https://github.com/user-attachments/assets/35e1ab02-aae6-4594-85ab-fd99c52d9c03)


6. **Demo PDF**
   - Example of a resume built using the resume builder feature.

   ![Resume PDF Screenshot](https://github.com/user-attachments/assets/75578e11-a0e4-41fa-961d-de6d8fcce5fb)


7. **Templates**
   - The following are screenshots of the six available templates for portfolio building:

   ![Template 1](https://github.com/user-attachments/assets/fac93a89-18eb-4ba5-be00-73dca010acd5)
   
   ![Template 2](https://github.com/user-attachments/assets/4ba71af0-49fb-4bb4-9e99-e5af67f557d1)
   
   ![Template 3](https://github.com/user-attachments/assets/7d8e9dab-52f1-4438-905d-9323aa73c4c4)
   
   ![Template 4](https://github.com/user-attachments/assets/3ae277cc-8723-4c03-b583-e2401f5a7e85)
   
   ![Template 5](https://github.com/user-attachments/assets/20e2c9da-42c3-4066-a0ed-e8542730ea5f)
   
   ![Template 6](https://github.com/user-attachments/assets/5a341a34-02fd-4d79-b25c-ca60c9027433)



## Database Details

The application uses MongoDB for data storage. It has two main collections:

1. **Users Collection**
   - Stores user details such as:
     - `fullName`: The user's full name
     - `email`: User's email address
     - `password`: Hashed password
     - `phone`: User's phone number
     - `createdAt`: Timestamp when the user was created
     - `updatedAt`: Timestamp when the user details were last updated
   - Security details such as salt for password hashing are also stored.

   ![Users Collection Screenshot](https://github.com/user-attachments/assets/d5d47417-a7af-46a0-a3ad-ccf71228c115)

2. **UserDatas Collection**
   - Stores user-submitted information for building resumes or portfolios, such as:
     - `firstname`: User's first name
     - `lastname`: User's last name
     - `email`: User's email address
     - `phone`: User's phone number
     - `skills`: List of skills
     - `aboutself`: About the user
     - `workexperience`: Details of work experience
     - `projectdetails`: Information about projects
     - `githublink`: GitHub profile link
     - `linkedinlink`: LinkedIn profile link
     - `achievements`: List of achievements
     - `profilepicture`: Path to the user's profile picture

   ![UserDatas Collection Screenshot](https://github.com/user-attachments/assets/7b5ddc6b-a48d-481b-bd69-6f44ecfc27ea)
   

## Setup and Installation

### Prerequisites

Before setting up the project, ensure you have the following installed:
- **Node.js** (Latest version)
- **MongoDB** (Local or remote instance)
- **NPM** (Node Package Manager)
- **A code editor** (e.g., Visual Studio Code)
- **A modern browser** (e.g., Chrome, Firefox)

### Installation Guide

1. **Clone the Repository**
   - Clone the project repository to your local machine:
     ```bash
     git clone https://github.com/KunvarAbhishek/Portfolio-Builder-No-Code.git
     cd Portfolio-Builder-No-Code
     ```

2. **Install Dependencies**
   - Navigate to the project directory using the terminal or command prompt:
     ```bash
     cd path_to_project
     ```
   - Install the required dependencies listed in the `package.json` file:
     ```bash
     npm install
     ```

3. **Set Up Environment Variables**
   - Look for a `.env.example` file in the project folder. If it exists, copy it to create a `.env` file:
     ```bash
     cp .env.example .env
     ```
   - Fill in the values in the `.env` file, such as the MongoDB connection string and any other required environment variables.

4. **Set Up MongoDB**
   - Ensure MongoDB is running. If you are using a local MongoDB instance, start the MongoDB service:
     ```bash
     mongosh
     ```

5. **Run the Project**
   - Start the Node.js application using one of the following commands:
     ```bash
     npm start
     ```
     or
     ```bash
     node index.js
     ```
      or
     ```bash
     npm i nodemon
     npm run dev
     ```


6. **Access the Application**
   - Once the application is running, open your browser and go to the URL specified in the project, typically:
     ```bash
     http://localhost:8000
     ```
     (Replace `8000` with the correct port if different.)



## Conclusion

This project allows users to build professional portfolios and resumes without any coding knowledge. It simplifies the process of creating web portfolios and resumes by providing customizable templates and an easy-to-use interface.

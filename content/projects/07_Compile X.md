+++
title = 'CompileX - Online Coding Platform' 
date = 2024-08-17T01:29:35+05:30
draft = false   
tags = ["Operating Systems","TypeScript"]
+++  
--- 

**CompileX** is a comprehensive online coding platform designed to empower developers of all skill levels. This platform offers a space to write and execute code, practice coding skills, and compete in coding contests.


## ✨ Features

### ⚔️ Coding Playground
- Write, compile, and execute code in a user-friendly editor.
- Support for at least one compiled language.
- Real-time error feedback and performance metrics.

### 🏋️‍♂️ Coding Arena
- Practice with pre-existing coding problems or upload new problems.
- Detailed problem descriptions, constraints, and test cases.
- Solutions can be tested against multiple test cases.

### 🎮 Coding Battleground
- Participate in ongoing contests and view real-time leaderboards.
- Create and host your own coding contests.

## 🛠️ Project Structure

The project is divided into two main parts: **Client** and **Server**.

### 🌐 Client
- **Components**: Reusable React components used throughout the platform.
- **Hooks**: Custom React hooks for managing state and effects.
- **Pages**: Individual pages for different parts of the application, such as the home page, login, signup, practice, contests, etc.
- **Assets**: Static assets like images and styles.

```
client/
│── src/
│   ├── assets/             
│   ├── Components/         
│   ├── Hooks/              
│   ├── Pages/              
│   ├── App.jsx             
│   ├── index.jsx           
│   └── ...                 
└── ...
```
### 🔧 Server
- **Codes**: Directory where user-submitted code is stored temporarily for execution.
- **Problems**: Contains JSON files that store coding problems and test cases.
- **Outputs**: Stores the outputs generated after code execution.
- **Scripts**: 
  - `executeCodeFile.js`: Executes the user-submitted code against provided test cases.
  - `generateCodeFile.js`: Generates the code file from the user's input.

```
server/
│── codes/                 
│── outputs/                
│── problems/               
│   ├── testcases/          
│   └── problems.json       
│── executeCodeFile.js      
│── generateCodeFile.js     
│── addProblems.js          
└── ...
```

## 🚀 Getting Started

### 📋 Prerequisites
- Node.js
- MongoDB (for storing user data and problems)
- Any code editor (e.g., Visual Studio Code)

### 💻 Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/pritpalcodes/CodeRaiders-Tally-Codebrewers-24
    ```

2. Navigate to the project directory:
    ```sh
    cd CodeRaiders-Tally-Codebrewers-24
    ```

3. Install dependencies for both Client and Server:
    ```sh
    cd Client
    npm install
    cd ../Server
    npm install
    ```

4. Set up your environment variables in the `Server/.env` file:
    ```env
    MONGODB_URI=<MONGODB_ATLAS_URI>
    ```

5. Run the development server:
    ```sh
    cd Client
    npm run dev
    cd ../Server
    npm start
    ```

6. Open the application in your browser:
    ```
    http://localhost:5173
    ```

## 🎯 Usage

- **Coding Playground**: Start coding by navigating to the Playground section.
- **Coding Arena**: Select a problem to solve or upload a new one.
- **Coding Battleground**: Join a contest or create your own.



## Project ScreenShots

![WhatsApp Image 2024-08-11 at 11 51 11](https://github.com/user-attachments/assets/8e352c16-de51-4422-864b-b0683255c965)
![WhatsApp Image 2024-08-11 at 11 51 30](https://github.com/user-attachments/assets/d826dd18-59f1-46ba-9435-2c85501d12d8)
![WhatsApp Image 2024-08-11 at 11 51 51](https://github.com/user-attachments/assets/8940da49-8a15-4ebf-87db-089416bb5d0c)
![WhatsApp Image 2024-08-11 at 11 52 45](https://github.com/user-attachments/assets/52e08582-e538-4496-ad8d-053b91d6acfb)
![WhatsApp Image 2024-08-11 at 11 53 15](https://github.com/user-attachments/assets/0203bf83-53b8-4f6b-8be2-0eb0a79a4250)
![WhatsApp Image 2024-08-11 at 11 53 57](https://github.com/user-attachments/assets/67a8cd68-c513-4d01-ab73-7fb7f41198c5)
![WhatsApp Image 2024-08-11 at 11 54 13](https://github.com/user-attachments/assets/a61d06c7-44e8-46c7-9fc1-3084535c24a9)
![WhatsApp Image 2024-08-11 at 11 54 31](https://github.com/user-attachments/assets/b5ce2b83-5180-4671-ae5f-76bf9bdf4eff)


# Blogging Platform

This is a simple blogging platform built using **Flask** and various web development tools. Users can create an account, log in, comment on posts, and admins can create, edit, and delete posts. The platform also integrates **Flask-SQLAlchemy** for database management, **Flask-Login** for user authentication, and **Flask-Bootstrap5** for responsive styling.

## Features

- **User Authentication**: Allows users to register, log in, and log out.
- **Post Creation & Management**: Admin users can create, edit, and delete blog posts.
- **Commenting**: General users can comment on posts.
- **Profile Images**: Gravatar integration displays profile images in the comment section.
- **Responsive Design**: The website is fully responsive and works well on both desktop and mobile devices.
  
## Tech Stack

- **Flask**: Lightweight web framework for building the application.
- **Flask-WTF**: For handling web forms.
- **Flask-Login**: For user authentication and session management.
- **Flask-SQLAlchemy**: For interacting with the SQLite database.
- **Flask-CKEditor**: For rich text editing in blog posts and comments.
- **Flask-Bootstrap5**: For styling the application using Bootstrap.
- **Flask-Gravatar**: For showing user profile images in the comment section.
- **SQLite**: Used for database storage (posts, users, and comments).
- **AWS EC2**: Deployed the application on an EC2 instance to make it publicly available.

## Project Setup

### Prerequisites

- Python 3.x
- pip (Python package manager)
- A GitHub account for managing the project

### Installation

1. **Clone the repository:**

   ```bash
   (https://github.com/DhanushGD/My-Blog.git)
   cd your-repository
2. **Create a virtual environment:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate  # For macOS/Linux
  venv\Scripts\activate     # For Windows
  Install the dependencies
  pip install -r requirements.txt
```
3. **Set up the environment variables:**
   - Set SECRET_KEY in your environment to keep your app secure.
   - Configure the SQLALCHEMY_DATABASE_URI to connect to your database.
   - For local development, SQLite is used, but you can change it to another database for production.

4. **Running Locally** 
   To run the application locally, execute:
    ```bash
       python app.py
- The app will be accessible at http://localhost:5000.

### Deploying to AWS EC2

1. **Launch an EC2 Instance:**
  - Go to the AWS EC2 console.
  - Create a new EC2 instance with Ubuntu or your preferred Linux distribution.
  - Ensure the instance has the necessary security group rules to allow HTTP traffic (port 80) and SSH access (port 22).
  - Connect to Your EC2 Instance:
  - Use SSH to connect to your EC2 instance:
  ```bash
  ssh -i your-key.pem ubuntu@your-ec2-public-ip
  ```
2. **Install Required Software:**
  Update the server and install required dependencies like Python, pip, and Git:
  ```bash
  sudo apt update
  sudo apt install python3-pip python3-venv git
  ```
3.**Clone the Repository:**
  On the EC2 instance, clone the project repository:
  ```bash
  https://github.com/DhanushGD/My-Blog.git
  cd your-repository
  ```
4. **Set up the Virtual Environment:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
```
5. **Install Dependencies:**
  ```bash
  pip install -r requirements.txt
```
6. **Run the Flask Application:**
Start the application:
```bash
python main.py
```
![image](https://github.com/user-attachments/assets/d4a4d14b-1234-46ea-b297-8c9a43e73817)

The application will be running and accessible through your EC2 instance's public IP address.

### Usage
  - User Registration: Users can register with an email and password.
    ![image](https://github.com/user-attachments/assets/64ba04b9-a63e-4a4e-babf-cc3c461292e4)

  - User Login: Registered users can log in to their accounts.
    ![image](https://github.com/user-attachments/assets/4224dc4b-6946-4978-80a0-3285f21d2df8)

  - Admin Dashboard: Admins can create, edit, and delete blog posts.
    ![image](https://github.com/user-attachments/assets/86f29aab-87b1-4f04-a135-e89678eab5c7)

  - Commenting: Logged-in users can comment on posts.
    ![image](https://github.com/user-attachments/assets/79ca5296-697a-44d9-acc3-1cd5c57dbdc5)

  - Profile Images: Gravatar is used to show profile images next to user comments.
  
### Contribution
  - Feel free to fork this repository and submit pull requests to enhance the functionality or improve the project. All contributions are welcome!





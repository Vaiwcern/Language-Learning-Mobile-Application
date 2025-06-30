# 📱 Language Learning Mobile Application

This is an Android application designed to help users practice all four essential language skills: **listening**, **speaking**, **reading**, and **writing**.  
It also includes features for **learning vocabulary** through interactive exercises and structured lessons.

The app is developed using **Java** with **Android Studio** for the frontend, and **Python Flask** with **MySQL** for the backend API and data management.

You can [📄 View the project report (PDF)](report.pdf) or ▶️ [Watch demo video on YouTube](https://youtu.be/ByzojncIdvE?si=ypMQmS76E8vLIM8r)

# 🏗️ Architecture

The application follows a **three-tier architecture** consisting of:

- A mobile frontend built with **Android Studio (Java/XML)**
- A backend server developed using **Python Flask**
- A **MySQL** relational database for persistent storage

---

### 📌 Overall System Architecture

The frontend includes a clean separation between UI, logic, and networking layers:

- **GUI (Layouts & XML)**: defines UI structure and style; dynamically updated on user interaction.
- **Controller (Activities/Fragments)**: manages app lifecycle, processes user input, calls service functions, and updates the UI based on backend responses.
- **Service layer**: sends HTTP requests to the backend and handles responses.

The backend is built with **Flask (Python)** following an MVC-like pattern:

- **Controllers (Routes)**: handle HTTP requests and route them to appropriate services.
- **Service layer**: processes logic, interacts with **SQLAlchemy**, and (optionally) external APIs.

The **MySQL database** is used to define tables, relationships, and store structured data. The schema is managed locally using **MySQL Workbench**.

<p align="center">
  <img src="assets/ArchitectureImages/architecture.png" alt="Architecture Diagram" width="700"/>
</p>

---

### 🖼️ System Tree

<p align="center">
  <img src="assets/ArchitectureImages/systemTree.png" alt="System Tree" width="700"/>
</p>



# ⚙️ Implementation

```bash
# 1. Clone the project
git clone https://github.com/your-username/your-repo.git

# 2. Create a virtual environment
py -m venv venv

# 3. Navigate to the server directory
cd 4lingo/server

# 4. Activate the virtual environment (on Windows)
.\venv\Scripts\activate

# 5. Install required dependencies
pip install -r requirements.txt

# 6. Set up MySQL database manually via MySQL Workbench:
#    - Use configuration in: server/config/config.py
#    - Run SQL script: server/database/queries/init.sql
#    - Make sure the DB is running and connected

# 7. Start the backend server
python server.py

# 8. Run the mobile app in Android Studio
#    - Open the 'client' folder
#    - Build and run on an emulator or real device

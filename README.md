# Digital Healthcare Management System

The Digital Healthcare Management System is a web-based platform that streamlines the management of healthcare services, including doctor information, patient bookings, and appointment management. Built using Flask and MySQL, the system facilitates seamless interaction between doctors, patients, and administrators.

---

## Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Database Schema](#database-schema)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)


---

## Features
- User Authentication (Signup/Login)
- Role-based Access (Doctor, Patient, Admin)
- Appointment Booking System
- Doctor and Patient Information Management
- Trigger-based Logs for Patient Updates and Deletions
- Search functionality for doctors by name or department

---

## Project Structure
```
.
├── hms.sql                 # Database schema, triggers, and sample data
├── requirements.txt        # Project dependencies
├── PROJECT/                # Main application folder
│   ├── main.py             # Main application file (placeholder)
│   ├── static/             # Static assets (CSS, JS, images)
│   └── templates/          # HTML templates
└── README.md               # Project documentation

```

---

## Installation

### Prerequisites
- Python 3.8+
- MySQL Server
- Flask and required dependencies

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/SreeDatta21/healthcare-management-system.git
   cd healthcare-management-system
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Import the database:
   - Open MySQL Workbench or any MySQL client.
   - Create a database named `hos`.
   - Import the `hms.sql` file into the `hos` database.
4. Configure database connection in `main.py`:
   ```python
   app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://<username>:<password>@localhost/hos'
   ```
5. Run the application:
   ```bash
   python main.py
   ```
6. Access the app in your browser at `http://127.0.0.1:5000/`.

---
![image](https://github.com/user-attachments/assets/726b2709-a1d1-4f80-8daf-4d12e3f1f73b)
## Usage
1. **Sign Up and Login**
   - Users can sign up as either a Doctor or Patient.
   - Login credentials are required to access the system.
![image](https://github.com/user-attachments/assets/82664f21-67f9-4f8f-a326-f66da4497f20)
2. **Manage Doctors**
   - Add doctor information, including email, name, and department.

3. **Book Appointments**
   - Patients can book appointments by selecting available slots and entering relevant details.
   - Validation ensures phone numbers are 10 digits long.
![image](https://github.com/user-attachments/assets/fdd7748d-cca3-4672-aff4-45bd3059231a)
4. **View Bookings**
   - Doctors can view all bookings.
   - Patients can view their personal bookings.
![image](https://github.com/user-attachments/assets/02e18459-b7c5-41d7-9c6a-d9bfd2bd8fe6)
5. **Edit and Delete Bookings**
   - Modify or remove existing bookings with triggers to log changes.

6. **Search Doctors**
   - Search for doctors by name or department.



---

## Database Schema

### Tables
- `doctors`: Stores doctor details.
- `patients`: Stores patient bookings.
- `user`: Stores user credentials and roles.
- `trigr`: Logs changes to patient bookings.
- `test`: Sample test table.

### Sample Schema
Refer to the `hms.sql` file for the complete database schema and sample data.

---

## Technologies Used
- **Backend:** Flask (Python), Flask-SQLAlchemy
- **Frontend:** HTML, CSS, JavaScript
- **Database:** MySQL
- **Authentication:** Flask-Login

---

## Contributing
Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m 'Add some feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.





# Smart AI Attendance System With Anti-Spoofing

A facial recognition based smart attendance system developed as part of my engineering studies in Information Technology. This project uses deep learning and computer vision to automate attendance marking with anti-spoofing protection.

---

##  Developer
**Shravani Sawant**  
B.E. Information Technology Student

---

##  About The Project
Traditional attendance systems are time-consuming and prone to proxy attendance. This system solves that problem by using **facial recognition** to automatically identify and mark attendance, with an **anti-spoofing model** to prevent fake attendance using photos or videos.

---

##  Features
-  Face detection and recognition using FaceNet
-  Anti-spoofing to prevent fake/proxy attendance
-  Employee management (Add, Update, Delete)
-  Attendance report generation
-  Automated email scheduler for daily reports
-  Desktop GUI built with Tkinter

---

##  Tech Stack
| Technology | Purpose |
|---|---|
| Python 3.6 | Core programming language |
| TensorFlow / Keras | Deep learning models |
| OpenCV | Face detection and video processing |
| FaceNet | Face embedding and recognition |
| MobileNet | Anti-spoofing model |
| MySQL (XAMPP) | Database for storing attendance |
| Tkinter | Desktop GUI |

---

##  Setup Instructions

### Prerequisites
- Anaconda
- XAMPP (for MySQL)
- Python 3.6

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/shravanisawant819/Smart-Attendance-System.git
cd Smart-Attendance-System
```

**2. Create and activate virtual environment**
```bash
conda create -n sams python=3.6
conda activate sams
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Setup Database**
- Open XAMPP Control Panel
- Start Apache and MySQL
- Go to `http://localhost/phpmyadmin`
- Create a database named `recognition`
- Run the following SQL:
```sql
CREATE TABLE login (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(50) NOT NULL
);

CREATE TABLE attendance (
    eid INT AUTO_INCREMENT PRIMARY KEY,
    department VARCHAR(50),
    fname VARCHAR(50),
    gender VARCHAR(10),
    contact_no VARCHAR(15),
    email_address VARCHAR(50),
    date_of_join VARCHAR(20)
);

CREATE TABLE report (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    date VARCHAR(20),
    time VARCHAR(20),
    status VARCHAR(20)
);

INSERT INTO login (username, password) VALUES ('admin', 'admin');
```

**5. Run the application**
```bash
python attendance_with_antispoofing.py
```

---

##  How To Use
1. **Login** with username: `admin` and password: `admin`
2. **Add Employee** — captures 50 face photos via webcam
3. **Extract Embeddings** — processes face photos into the model
4. **Train the System** — trains the face recognition model
5. **Face Recognizer** — marks attendance automatically
6. **Attendance Report** — view and search attendance records

---

##  What I Learned
- How facial recognition works using FaceNet embeddings
- Anti-spoofing techniques using MobileNet deep learning model
- Integrating Python applications with MySQL database
- Building desktop GUI applications with Tkinter
- Setting up and running deep learning models locally
- Virtual environment management with Anaconda

---

##   project screenshots
<img width="1631" height="915" alt="Screenshot 2026-06-09 145557" src="https://github.com/user-attachments/assets/47548705-cf9a-42d2-ab2e-1a70ae0c464a" />
<img width="1683" height="913" alt="Screenshot 2026-06-09 145620" src="https://github.com/user-attachments/assets/2208e8c3-5a71-4317-87ee-fc71cd8cf8f7" />
<img width="1682" height="915" alt="Screenshot 2026-06-09 145832" src="https://github.com/user-attachments/assets/6a778fef-cb48-4e52-8e14-ceabc2da9d3f" />
<img width="1686" height="909" alt="Screenshot 2026-06-09 145910" src="https://github.com/user-attachments/assets/34365378-56ae-4991-a434-37bcb52543c7" />
<img width="1416" height="891" alt="Screenshot 2026-06-09 145919" src="https://github.com/user-attachments/assets/ec6ee7f4-a449-4191-aa66-23d592836a2a" />
<img width="1751" height="911" alt="Screenshot 2026-06-09 145934" src="https://github.com/user-attachments/assets/78e887fc-eace-4168-927c-a506689ca433" />
<img width="1711" height="921" alt="Screenshot 2026-06-09 150012" src="https://github.com/user-attachments/assets/59949066-b560-4007-b6fd-79278b49874a" />









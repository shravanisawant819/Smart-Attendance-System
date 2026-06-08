# 🎓 Smart AI Attendance System With Anti-Spoofing

A facial recognition based smart attendance system developed as part of my engineering studies in Information Technology. This project uses deep learning and computer vision to automate attendance marking with anti-spoofing protection.

---

## 👩‍💻 Developer
**Shravani Sawant**  
B.E. Information Technology Student

---

## 📌 About The Project
Traditional attendance systems are time-consuming and prone to proxy attendance. This system solves that problem by using **facial recognition** to automatically identify and mark attendance, with an **anti-spoofing model** to prevent fake attendance using photos or videos.

---

## ✨ Features
- 👤 Face detection and recognition using FaceNet
- 🛡️ Anti-spoofing to prevent fake/proxy attendance
- 🗄️ Employee management (Add, Update, Delete)
- 📊 Attendance report generation
- 📧 Automated email scheduler for daily reports
- 🖥️ Desktop GUI built with Tkinter

---

## 🛠️ Tech Stack
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

## ⚙️ Setup Instructions

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

## 🚀 How To Use
1. **Login** with username: `admin` and password: `admin`
2. **Add Employee** — captures 50 face photos via webcam
3. **Extract Embeddings** — processes face photos into the model
4. **Train the System** — trains the face recognition model
5. **Face Recognizer** — marks attendance automatically
6. **Attendance Report** — view and search attendance records

---

## 📚 What I Learned
- How facial recognition works using FaceNet embeddings
- Anti-spoofing techniques using MobileNet deep learning model
- Integrating Python applications with MySQL database
- Building desktop GUI applications with Tkinter
- Setting up and running deep learning models locally
- Virtual environment management with Anaconda

---

## 📷 Screenshots
*(Add screenshots of your running application here)*

---

## 📄 License
This project is based on open source work and is intended for educational purposes.

# CareConnect — Healthcare Coordination Platform

<div align="center">

**A web-based platform that empowers patients and families to make fast, informed decisions about hospital selection and ambulance services during medical emergencies.**

[![Django](https://img.shields.io/badge/Django-4.2.7-092E20?style=flat&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?style=flat&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-Educational-blue.svg)](#license)

</div>

---

## 🌟 Overview

CareConnect bridges the gap between patients and healthcare providers by offering real-time visibility into hospital bed availability, facilities, pricing, and ambulance services — all in one place. Designed to reduce confusion and delays during medical emergencies, it serves three types of users: patients/families, hospital admins, and ambulance providers.

---

## ✨ Key Features

- 🏥 **Hospital Search & Comparison** — Find and compare hospitals by location, facilities, and real-time bed availability
- 🚑 **Ambulance Directory** — Browse ambulance services with transparent pricing and service area maps
- 📊 **Role-based Dashboards** — Dedicated dashboards for hospital administrators and ambulance providers
- 💰 **Transparent Pricing** — Detailed pricing for hospital services and ambulance rates
- 🛏️ **Live Bed Availability** — Real-time updates on general, ICU, and emergency beds
- 🔐 **Custom Authentication** — Secure role-based login with OTP verification
- 📋 **Activity Logs** — Full audit trail for hospital and ambulance admin actions

---

## 📸 Screenshots

### Landing Page, Sign In & Sign Up

<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/landing_page.png" alt="Landing Page" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/signup_page.png" alt="Sign Up Page" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/signin_page.png" alt="Sign In Page" width="100%">

### User Dashboard

<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/user_hospital_search.png" alt="Hospital Search" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/user_hospital_results.png" alt="Hospital Results" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/user_hospital_comparison.png" alt="Hospital Comparison" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/user_ambulance_directory.png" alt="Ambulance Directory" width="100%">

### Hospital Admin Dashboard

<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/hospital_update_beds.png" alt="Update Bed Availability" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/hospital_update_facilities.png" alt="Update Facilities" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/hospital_update_insurance.png" alt="Update Insurance" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/hospital_update_pricing.png" alt="Update Pricing" width="100%">

### Ambulance Provider Dashboard

<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/ambulance_dashboard_overview.png" alt="Dashboard Overview" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/ambulance_manage_fleet.png" alt="Manage Fleet" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/ambulance_fleet_list.png" alt="Fleet List" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/ambulance_service_area.png" alt="Service Area" width="100%">
<img src="https://github.com/salmanmemon11/Care-Connect/blob/main/screenshots/ambulance_update_pricing.png" alt="Update Pricing" width="100%">

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | Django 4.2.7, Python 3.x |
| Database | SQLite3 |
| Auth | Custom role-based authentication with OTP |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/salmanmemon11/Care-Connect.git
   cd Care-Connect
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv venv

   # Windows
   venv\Scripts\activate

   # macOS / Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Open .env and fill in your configuration (see below)
   ```

5. **Run database migrations**
   ```bash
   python manage.py migrate
   ```

6. **Start the development server**
   ```bash
   python manage.py runserver
   ```

7. **Open in browser**
   ```
   http://localhost:8000
   ```

### Environment Variables

Copy `.env.example` to `.env` and configure:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True

# Email (for OTP / notifications)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-app-password
```

> ⚠️ Never commit your `.env` file. It is already listed in `.gitignore`.

---

## 👥 User Roles

| Role | Capabilities |
|---|---|
| **General User** | Search hospitals, compare facilities, browse ambulance services |
| **Hospital Admin** | Manage bed availability, facilities, pricing, and insurance providers |
| **Ambulance Provider** | Manage fleet, update service areas and pricing |

---

## 📁 Project Structure

```
careconnect/
├── manage.py
├── requirements.txt
├── .env.example
├── careconnect/          # Project settings & URL config
├── core/                 # Authentication, OTP, landing pages
├── hospital/             # Hospital admin views & templates
├── ambulance/            # Ambulance provider views & templates
├── userapp/              # Patient/user-facing search & compare
└── static/               # CSS, JavaScript, images
    ├── css/
    ├── js/
    └── images/screenshots/
```

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project was developed for **educational purposes**.

---

<div align="center">

Developed by **[Salman Memon](https://github.com/salmanmemon11)** and team

**Made with ❤️ for better healthcare coordination**

</div>

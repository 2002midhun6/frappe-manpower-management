# Manpower Allocation System

A custom manpower allocation system built using the **Frappe Framework**, **ERPNext**, and **HRMS**. The project aims to manage employees, customers, projects, and manpower assignments in one centralized system.

## 🚀 Project Overview

The Manpower Allocation System is designed to simplify employee management and workforce allocation. It integrates HR-related functionality with customer and project management to help organizations allocate the right employees to the right projects.

## 🛠️ Tech Stack

- **Framework:** Frappe Framework v16
- **ERP System:** ERPNext v16
- **HR Management:** Frappe HRMS v16
- **Backend:** Python
- **Frontend:** JavaScript, HTML, CSS
- **Database:** MariaDB
- **Version Control:** Git and GitHub

## ✨ Features

- Employee and workforce management using HRMS.
- Customer and business relationship management using CRM/ERPNext functionality.
- Custom Manpower Allocation DocType.
- Employee assignment to projects or customer requirements.
- Integration with existing Frappe and HRMS functionality.
- Centralized management of manpower allocation records.

## 📁 Project Structure

```text
frappe-bench/
├── apps/
│   ├── frappe/
│   ├── erpnext/
│   ├── hrms/
│   └── manpower_management/
│       └── manpower_management/
│           ├── doctype/
│           │   └── manpower_allocation/
│           ├── hooks.py
│           └── ...
├── sites/
└── README.md
```

*Note: This is a simplified structure. The actual structure may vary depending on your implementation.*

## ⚙️ Prerequisites

Make sure you have the following installed:

- Python
- Node.js and npm
- MariaDB
- Redis
- Frappe Bench
- Git

## 📦 Installation

### 1. Clone the repository

Clone your custom app repository into your existing Frappe Bench environment.

```bash
cd frappe-bench
bench get-app https://github.com/2002midhun6/manpower_management.git
```

Replace the URL with the GitHub repository that contains your custom app.

### 2. Create a site

If you do not already have a site, create one:

```bash
bench new-site manpower.localhost
```

### 3. Install required apps

Install the applications on your site:

```bash
bench --site manpower.localhost install-app erpnext
bench --site manpower.localhost install-app hrms
bench --site manpower.localhost install-app manpower_management
```

If you use the separate Frappe CRM application, install it as well, following its official installation instructions.

### 4. Run database migrations

```bash
bench --site manpower.localhost migrate
```

### 5. Start the development server

```bash
bench start
```

Open the site in your browser:

```text
http://manpower.localhost:8000
```

## 🔧 Development

After modifying DocTypes, Python files, or JavaScript files, run the necessary migration and cache-clearing commands.

```bash
bench --site manpower.localhost migrate
bench --site manpower.localhost clear-cache
```

Restart the development server if necessary.

## 🧪 Testing

Run the following command to execute tests for the custom app:

```bash
bench --site manpower.localhost run-tests --app manpower_management
```

Ensure the app's tests and required dependencies are configured before running the command.

## 🔐 Configuration

- Keep database credentials and other secrets out of Git.
- Do not commit private site configuration files.
- Use environment variables or appropriate Frappe configuration for sensitive settings.
- Avoid committing generated files, logs, backups, and the Python virtual environment.

## 🗺️ Future Improvements

- Employee availability tracking.
- Skill-based manpower allocation.
- Project-wise workforce planning.
- Allocation status and approval workflow.
- Employee workload monitoring.
- Reports and dashboards for utilization and allocation history.

## 🤝 Contributing

Contributions and suggestions are welcome. Fork the repository, create a feature branch, make your changes, and submit a pull request.

## 📄 License

Add the appropriate license for your project before distributing it publicly.

---

**Built with Frappe Framework, ERPNext, and HRMS.**

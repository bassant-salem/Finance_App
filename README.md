# 💰 Personal Finance Management System

A comprehensive ASP.NET Core MVC web application designed to help users take control of their financial health through income tracking, expense management, budget planning, and goal setting.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![.NET](https://img.shields.io/badge/.NET-8.0-purple.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

## 📋 Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Database Schema](#database-schema)
- [What I Learned](#what-i-learned)
- [Future Enhancements](#future-enhancements)
- [Contact](#contact)

## ✨ Features

### Core Functionality
- **📊 Dashboard**: Visual overview of financial status with charts and statistics
- **💸 Expense Tracking**: Categorize and monitor all expenses with detailed records
- **💵 Income Management**: Track multiple income sources and payment schedules
- **🎯 Budget Planning**: Set monthly/yearly budgets and monitor spending against targets
- **🏆 Financial Goals**: Define and track progress towards savings goals
- **📈 Reports & Analytics**: Generate insights with visual charts and spending trends

### User Experience
- **🔐 Secure Authentication**: User registration and login with ASP.NET Identity
- **📱 Responsive Design**: Mobile-friendly interface using Bootstrap
- **🔍 Advanced Filtering**: Search and filter transactions by date, category, amount
- **📅 Date Range Selection**: View financial data for custom time periods
- **📊 Category Management**: Custom expense/income categories

## 🛠️ Tech Stack

### Backend
- **Framework**: ASP.NET Core 8.0 MVC
- **Language**: C# 12
- **ORM**: Entity Framework Core 8.0
- **Database**: SQL Server 2022
- **Authentication**: ASP.NET Core Identity

### Frontend
- **View Engine**: Razor Pages
- **CSS Framework**: Bootstrap 5
- **JavaScript**: jQuery, Chart.js
- **Icons**: Font Awesome

### Tools & Practices
- **IDE**: Visual Studio 2022
- **Version Control**: Git & GitHub
- **Design Patterns**: Repository Pattern, MVC, Dependency Injection
- **Code Quality**: SOLID Principles, Clean Architecture

## 📸 Screenshots
  ![Finance_App](https://github.com/user-attachments/assets/922b03f3-3ee0-41c1-a698-8ee08877625c)


## 🚀 Getting Started

### Prerequisites
- .NET 8.0 SDK or later
- SQL Server 2019 or later (or SQL Server Express)
- Visual Studio 2022 / VS Code / JetBrains Rider

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/bassant-salem/Finance_App.git
cd Finance_App
```

2. **Update Database Connection**
Open `appsettings.json` and update the connection string:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=FinanceAppDB;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
```

3. **Apply Database Migrations**
```bash
dotnet ef database update
```

4. **Run the Application**
```bash
dotnet run
```

5. **Access the App**
Navigate to `https://localhost:5001` in your browser

### Quick Start with Sample Data
```bash
# Seed the database with sample categories and demo data
dotnet run --seed-data
```

## 🗄️ Database Schema

### Key Entities
- **User**: Application users with authentication
- **Transaction**: Income and expense records
- **Category**: Transaction categories (Groceries, Salary, Rent, etc.)
- **Budget**: Monthly/yearly budget allocations
- **Goal**: Financial goals and progress tracking

### Relationships
- One User → Many Transactions
- One Category → Many Transactions
- One User → Many Budgets
- One User → Many Goals

```
┌─────────┐         ┌──────────────┐         ┌──────────┐
│  User   │────────▶│ Transaction  │◀────────│ Category │
└─────────┘         └──────────────┘         └──────────┘
     │                                             
     │              ┌──────────┐                   
     ├─────────────▶│  Budget  │                   
     │              └──────────┘                   
     │                                             
     │              ┌──────────┐                   
     └─────────────▶│   Goal   │                   
                    └──────────┘                   
```

## 📚 What I Learned

This project strengthened my skills in:

### Technical Skills
- **ASP.NET Core MVC**: Building scalable web applications following MVC pattern
- **Entity Framework Core**: Code-First approach, migrations, and LINQ queries
- **SQL Server**: Database design, normalization, and complex queries
- **Authentication & Security**: Implementing ASP.NET Identity, authorization policies
- **Frontend Integration**: Razor syntax, JavaScript interop, responsive design

### Software Engineering Practices
- **Repository Pattern**: Abstracting data access for cleaner, testable code
- **SOLID Principles**: Writing maintainable and extensible code
- **Dependency Injection**: Loosely coupled architecture
- **Error Handling**: Comprehensive validation and exception management
- **Version Control**: Git workflow with meaningful commits

### Problem-Solving
- Designing normalized database schema for financial data
- Implementing complex LINQ queries for financial analytics
- Creating dynamic charts with Chart.js for data visualization
- Handling date ranges and currency formatting across different cultures
- Optimizing queries to prevent N+1 problems with eager loading

## 🔮 Future Enhancements

- [ ] **Multi-Currency Support**: Track finances in different currencies
- [ ] **Recurring Transactions**: Auto-generate monthly bills and income
- [ ] **Export Reports**: PDF/Excel export functionality
- [ ] **Email Notifications**: Budget alerts and reminders
- [ ] **Mobile App**: React Native or .NET MAUI companion app
- [ ] **Bank Integration**: Automatic transaction imports (Plaid API)
- [ ] **Investment Tracking**: Stock and crypto portfolio management
- [ ] **AI Insights**: Smart spending recommendations using ML.NET
- [ ] **Multi-User**: Household shared budgets and expenses
- [ ] **Dark Mode**: Theme customization options

## 🧪 Testing

Run unit tests:
```bash
dotnet test
```

> **Note**: Currently implementing unit tests using xUnit and Moq for business logic

## 📝 Code Quality

- **Code Coverage**: [Add coverage percentage when implemented]
- **Code Standards**: Following C# coding conventions
- **Documentation**: XML comments on public methods
- **Error Handling**: Comprehensive try-catch blocks and custom error pages

## 🤝 Contributing

This is a personal learning project, but suggestions and feedback are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**Bassant Salem**
- 🎓 Computer Science Graduate - Ain Shams University
- 💼 Aspiring .NET Developer
- 📧 Email: [your.email@example.com]
- 💼 LinkedIn: [Your LinkedIn Profile]
- 🌐 Portfolio: [Your Portfolio Website if you have one]

## 🙏 Acknowledgments

- ASP.NET Core documentation and community
- Bootstrap for responsive design framework
- Chart.js for beautiful data visualizations
- Stack Overflow community for problem-solving support

---

⭐ If you found this project helpful or interesting, please consider giving it a star!

**Status**: ✅ Fully Functional | 🚀 Actively Maintained | 📚 Learning Project

*Built with ❤️ using ASP.NET Core*

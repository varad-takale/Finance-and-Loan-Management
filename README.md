# Finance & Loan Management System (MAVKAR Finance)

A desktop application for a finance company to manage customer loan enquiries, built with **Java Swing**, with **JDBC / MySQL** as the planned data layer.

> **Project status: work in progress.** The screens and navigation are built. Connecting them to the MySQL database (saving, deleting, updating and listing enquiries) and the loan features are the next steps, listed in the roadmap below.

<!-- Add screenshots here: put images in a /screenshots folder, then add lines like
![Main menu](screenshots/main-menu.png)
![Enquiry form](screenshots/enquiry-form.png)
-->

## Current status

| Area | Status |
|---|---|
| Main menu screen ("MAVKAR FINANCE") with Add Enquiry and Delete Enquiry options | Done |
| Enquiry form (customer and income details) | Screen built |
| Delete Enquiry screen (lookup by mobile number) | Screen built |
| MySQL connection class (`DAO.java`) | Written |
| Saving enquiries to the database | Not yet connected |
| Deleting enquiries from the database | Not yet connected |
| Update Record, Display All, Loan Services | Menu options only, not implemented |

## Enquiry form fields

The enquiry form collects: cash ID, name, mobile number, email, address, service type (self-employed or job), company/business name, annual income, past loan (yes/no) and PAN card number.

## Tech stack

- **Language:** Java
- **UI:** Java Swing / AWT
- **Database (planned):** MySQL through JDBC (`DAO.java` targets a local database named `alldata`)

## Getting started

### Prerequisites

- JDK 8 or newer

MySQL and the MySQL Connector/J JAR are only needed once the database features are connected.

### Run it

```bash
git clone https://github.com/varad-takale/Finance-and-Loan-Management.git
cd Finance-and-Loan-Management
javac *.java
java frame_1
```

`frame_1` is the entry point and opens the **MAVKAR FINANCE** main menu.

## Project structure

| File | Purpose |
|---|---|
| `frame_1.java` | Main menu and entry point |
| `add_enquiry.java` | Enquiry form screen |
| `Delete_Enquiry.java` | Delete enquiry screen (mobile number lookup) |
| `deleteconf.java` | Confirmation screen |
| `DAO.java` | MySQL/JDBC connection class |
| `DeleteFromDatabase.java` | Database delete logic (to be connected) |

## Roadmap

- [ ] Save enquiries to MySQL (create the table and the insert query)
- [ ] Delete an enquiry by mobile number, with confirmation
- [ ] Update Record and Display All screens
- [ ] EMI calculator (principal, interest rate, tenure) and repayment schedule
- [ ] Loan status tracking for each enquiry
- [ ] Move database credentials to a config file
- [ ] Input validation (mobile number, email, PAN format)
- [ ] Group the code into packages and add a build tool (Maven)

## Author

**Varad Takale** | [GitHub](https://github.com/varad-takale)

```markdown
# 📋 Ednex Consultant Management System v2.0
### *Professional Single-File Web Application — Feature Documentation*

---

> **Built for:** Ednex Consultant (Peshawar)
> **CEO:** Asfandyar Rabbani Advocate
> **Developer:** Humam Khalil | [humamkhalil.netlify.app](https://humamkhalil.netlify.app)
> **Tech Stack:** Pure HTML5 · CSS3 · Vanilla JavaScript · localStorage + CSV
> **Type:** Single `.html` file — runs directly in any modern browser

---

## 📑 Table of Contents

1. [Overview](#overview)
2. [Getting Started](#getting-started)
3. [Authentication & Roles](#authentication--roles)
4. [Dashboard](#dashboard)
5. [Client Management](#client-management)
6. [Applications](#applications)
7. [Cases Management](#cases-management)
8. [Appointments](#appointments)
9. [WhatsApp Messaging](#whatsapp-messaging)
10. [Foreign Education Module](#foreign-education-module)
11. [Religious Services Module](#religious-services-module)
12. [All Services](#all-services)
13. [User Management](#user-management)
14. [Social Links Management](#social-links-management)
15. [Data Management](#data-management)
16. [Backup & Recovery](#backup--recovery)
17. [Settings & Customization](#settings--customization)
18. [UI/UX Features](#uiux-features)
19. [Developer Information](#developer-information)
20. [Technical Notes](#technical-notes)
21. [Keyboard Shortcuts](#keyboard-shortcuts)
22. [Limitations & Notes](#limitations--notes)

---

## Overview

The **Ednex Consultant Management System v2.0** is a fully featured,
browser-based management portal built into a **single `.html` file**.
It requires no internet connection, no server, no installation, and no
external dependencies. Simply open the file in a browser and start working.

It is designed specifically for **Ednex Consultant (Peshawar)** — a
legal and business consultancy firm led by **Asfandyar Rabbani Advocate**
— to manage clients, cases, applications, appointments, religious service
bookings, foreign education consulting, WhatsApp communication, and more.

---

## Getting Started

```
1. Download or copy the single .html file
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari)
3. Log in using your credentials (see below)
4. Start managing your consultancy data
```

> ⚡ **No installation required.**
> ⚡ **No internet needed** (except for WhatsApp sending and map/social links).
> ⚡ **All data is saved** in the browser's localStorage automatically.

---

## Authentication & Roles

The system uses a **3-tier Role-Based Access Control (RBAC)** system.
All content is protected behind a login screen.

### 🔐 Login Credentials

| Username  | Password    | Role          |
|-----------|-------------|---------------|
| `ADMIN`   | `asdf123`   | Admin         |
| `SUPER`   | `super@123` | Super Admin   |
| `GENERAL` | `gen@123`   | General User  |

---

### 👥 Role Permissions

| Feature / Page            | General | Admin | Super Admin |
|---------------------------|:-------:|:-----:|:-----------:|
| Dashboard                 | ✅      | ✅    | ✅          |
| Clients                   | ✅      | ✅    | ✅          |
| Appointments              | ✅      | ✅    | ✅          |
| Services                  | ✅      | ✅    | ✅          |
| Religious Services        | ✅      | ✅    | ✅          |
| Foreign Education         | ✅      | ✅    | ✅          |
| Applications              | ❌      | ✅    | ✅          |
| Cases                     | ❌      | ✅    | ✅          |
| WhatsApp Messaging        | ❌      | ✅    | ✅          |
| Social Links Management   | ❌      | ✅    | ✅          |
| Data Management           | ❌      | ✅    | ✅          |
| Backup & Recovery         | ❌      | ✅    | ✅          |
| Settings                  | ❌      | ✅    | ✅          |
| User Management           | ❌      | ❌    | ✅          |
| Reset Other Users' Passwords | ❌   | ❌    | ✅          |

---

### 🔑 Session Handling

- Sessions are stored in `localStorage`
- Refreshing the page **keeps you logged in**
- Clicking **Logout** clears the session
- Each user can **change their own password** from Settings
- Only **Super Admins** can reset other users' passwords

---

## Dashboard

The central hub of the application. Displays a real-time overview
of all consultancy data.

### What you can do:
- 📊 View **4 live stat cards**:
  - Total Clients (with active count)
  - Total Cases (with open count)
  - Total Applications (with pending count)
  - Total Appointments (with today's count)
- 👋 See a **time-aware greeting** (Good Morning / Afternoon / Evening)
- 🏛️ View **CEO information** — Asfandyar Rabbani Advocate
- 🔗 Access **quick links**:
  - Official Facebook Page
  - CEO Facebook Profile
  - Google Maps Location
- ⚡ Use **Quick Action buttons**:
  - Add New Client
  - Book Appointment
  - Open WhatsApp Messaging
  - Download Full Backup
- 👥 See **Recent Clients** mini-list with name, phone, type, and status

---

## Client Management

Manage all consultancy clients in a structured table with full
CRUD (Create, Read, Update, Delete) capabilities.

### What you can do:
- ➕ **Add new clients** with a detailed form
- ✏️ **Edit existing client** records inline
- 🗑️ **Delete clients** with a confirmation prompt
- 🔍 **Search / filter** clients in real time by any field
- 💬 **Quick WhatsApp** button per client — opens the messaging page
  with the client's number pre-filled
- 📥 **Export clients** to a `.csv` file

### Client Record Fields:
| Field       | Description                        |
|-------------|------------------------------------|
| Full Name   | Client's complete name             |
| Phone       | Contact phone number               |
| Email       | Email address                      |
| Type        | Individual / Corporate / Business / NGO |
| Status      | Active / Pending / Inactive        |
| Address     | Physical address                   |
| Date Joined | When the client was onboarded      |
| Notes       | Any additional notes               |

---

## Applications

Track all client visa, permit, and admission applications.

### What you can do:
- ➕ **Create new applications** with full details
- ✏️ **Edit** application records
- 🗑️ **Delete** applications
- 🔍 **Search** across all application fields
- 📌 **Set priority universities** (1st, 2nd, 3rd choice)
- 📥 **Export** to CSV

### Application Record Fields:
| Field               | Description                              |
|---------------------|------------------------------------------|
| Application #       | Unique reference number                  |
| Client Name         | Linked client                            |
| Application Type    | Student Visa / Work Permit / Family Visa / Tourist Visa / PR / Business Visa |
| Country             | Target country                           |
| University          | Institution (if applicable)              |
| 1st Priority        | First choice university                  |
| 2nd Priority        | Second choice university                 |
| 3rd Priority        | Third choice university                  |
| Status              | Draft / Submitted / In Review / Approved / Rejected / On Hold |
| Submission Date     | Date of application submission           |

---

## Cases Management

Manage all legal and consultancy cases from opening to closure.

### What you can do:
- ➕ **Add new cases** with detailed information
- ✏️ **Edit** case details as they progress
- 🗑️ **Delete** closed or erroneous cases
- 🔍 **Real-time search** across all fields
- 🏷️ **Priority tagging** — High / Medium / Low
- 📊 **Status tracking** — Open → In Progress → On Hold → Closed
- 📥 **Export** cases to CSV

### Case Record Fields:
| Field       | Description                                    |
|-------------|------------------------------------------------|
| Case #      | Unique case identifier (e.g., EC-2024-001)     |
| Client      | Client associated with the case                |
| Title       | Brief description of the case                  |
| Type        | Corporate / Immigration / Documentation / Legal / Civil / Criminal / Family |
| Status      | Open / In Progress / On Hold / Closed / Dismissed |
| Priority    | High / Medium / Low                            |
| Assigned To | Responsible person (e.g., Asfandyar Rabbani)  |
| Date Opened | When the case was opened                       |
| Notes       | Case notes and updates                         |

---

## Appointments

Schedule and manage all client appointments.

### What you can do:
- ➕ **Book new appointments** with date and time
- ✏️ **Edit** existing appointment details
- 🗑️ **Delete** appointments
- 🔍 **Search** appointments by client, service, or date
- 🏷️ **Status tracking** — Pending / Confirmed / Completed / Cancelled / Tentative
- 📅 **Today's count** visible on the Dashboard stat card
- 📥 **Export** appointments to CSV

### Appointment Record Fields:
| Field   | Description                          |
|---------|--------------------------------------|
| Client  | Client's name                        |
| Service | Service requested                    |
| Date    | Appointment date                     |
| Time    | Appointment time                     |
| Status  | Pending / Confirmed / Completed / Cancelled / Tentative |
| Notes   | Additional notes                     |

---

## WhatsApp Messaging

Send messages directly to clients via WhatsApp using the
consultancy's official number.

### What you can do:
- 📋 **Select a client** from the dropdown — phone number auto-fills
- ✍️ **Manually enter** any WhatsApp number
- 📝 **Choose from message templates**:
  - Appointment Reminder
  - Documents Required
  - Visa Ready
  - Follow Up
  - Custom Message
- 💬 **Send message** — opens WhatsApp Web/App with pre-filled text
- 📋 **Message log** — view the last 50 messages sent (client, number, time, preview)
- ⚙️ **Configure official number** from Settings page
- 💬 **Quick-send** from the Clients table via the WhatsApp button

### How WhatsApp Sending Works:
```
1. Admin selects client or enters a number manually
2. Admin chooses a template or types a custom message
3. Clicking "Send via WhatsApp" opens wa.me link in a new tab
4. Message is pre-filled — admin just hits Send in WhatsApp
5. The message is logged automatically in the Message Log
```

> 📌 Messages are sent **from** the configured official
> consultancy WhatsApp number (set in Settings).

---

## Foreign Education Module

A dedicated module for managing foreign university applications
and education consulting.

### What you can do:

#### 🌍 Country Management
- ➕ **Add countries** with flag emoji and a list of universities
- ❌ **Remove countries** with one click
- 🏛️ **View universities** per country in ranked order

#### 🏛️ University Finder
- Select any configured country to instantly view its
  universities in ranked order (1st, 2nd, 3rd…)

#### 📌 Priority-Based Applications
- Create education applications with structured priority selection:
  - **1st Priority University**
  - **2nd Priority University**
  - **3rd Priority University**
- Track application status (Draft → Submitted → Offer Received → Enrolled)
- Edit and delete education applications

### Pre-loaded Countries (Sample Data):
| Country        | Sample Universities                           |
|----------------|-----------------------------------------------|
| 🇬🇧 UK         | Oxford, Cambridge, Imperial, Edinburgh        |
| 🇨🇦 Canada     | Toronto, McGill, UBC, Waterloo                |
| 🇦🇺 Australia  | ANU, Melbourne, Sydney                        |
| 🇩🇪 Germany    | TU Munich, LMU, Heidelberg                    |
| 🇲🇾 Malaysia   | Universiti Malaya, UPM, UKM                   |

---

## Religious Services Module

Organized management of all Hajj, Umrah, Ziyarat, and
air ticket services offered by the consultancy.

### What you can do:
- 📂 View services organized into **collapsible categories**
- 💬 **Inquire** about any service — opens WhatsApp Messaging
- ➕ **Book new religious service** with client details
- ✏️ **Edit** existing bookings
- 🗑️ **Delete** bookings
- 📥 **Export** religious bookings to CSV

### Service Categories:

#### 🕋 Hajj Services
- Hajj Registration Assistance
- Hajj Package Booking (Economy / Standard / VIP)
- Mahram Documentation

#### 🕌 Umrah Services
- Umrah Visa Processing
- Umrah Package Booking (Group & Individual)
- Hotel & Transport Booking (Makkah & Madinah)

#### ✈️ Air Ticket Services
- Domestic Air Tickets (PIA, Airblue, Serene Air)
- International Air Tickets (All major airlines)
- Ticket Reissuance & Refunds

#### 🌹 Ziyarat & Travel
- Ziyarat Tours
- Iran & Iraq Ziyarat Packages
- Travel Documentation

### Booking Record Fields:
| Field        | Description                                          |
|--------------|------------------------------------------------------|
| Client Name  | Client's full name                                   |
| Phone        | Contact number                                       |
| Service Type | Hajj / Umrah / Ziyarat / Air Ticket / Hotel / Transport |
| Package      | Economy / Standard / Premium / VIP                   |
| Year         | Year of service (e.g., 2025)                         |
| Status       | Inquiry / Registered / Confirmed / Completed / Cancelled |
| Notes        | Any additional notes                                 |

---

## All Services

Manage the complete catalogue of services offered by Ednex Consultant.

### What you can do:
- ➕ **Add new services** to the catalogue
- ✏️ **Edit** service details and pricing
- 🗑️ **Delete** discontinued services
- 🔍 **Search** services by name, category, or status
- 📥 **Export** services to CSV

### Service Record Fields:
| Field       | Description                                         |
|-------------|-----------------------------------------------------|
| Name        | Service name                                        |
| Category    | Immigration / Corporate / Documentation / Legal / Finance / Religious / Education / Other |
| Price (PKR) | Service fee in Pakistani Rupees                     |
| Duration    | Estimated duration (e.g., "2 hours", "1 week")      |
| Status      | Available / Coming Soon / Discontinued              |
| Description | Detailed service description                        |

---

## User Management

> 🔒 **Super Admin only**

Manage system users, roles, and passwords.

### What Super Admins can do:
- ➕ **Add new users** with role assignment
- ✏️ **Edit** user details and roles
- 🗑️ **Delete** users
- 🔑 **Reset any user's password** instantly
- 🏷️ **Assign roles**: General / Admin / Super Admin

### User Record Fields:
| Field    | Description                          |
|----------|--------------------------------------|
| Name     | User's full name                     |
| Username | Login username                       |
| Password | Account password                     |
| Role     | general / admin / super              |
| Initials | 2-character avatar initials (e.g., AD) |

> 👤 **General and Admin users** can view the Users page
> but cannot make changes — read-only with an access notice.

---

## Social Links Management

Dynamically manage all social media and contact links
displayed throughout the application.

### What you can do:
- ➕ **Add new social links** (any platform)
- ✏️ **Edit** existing links
- 🗑️ **Delete** links that are no longer needed
- 🌐 **Open links** directly in a new browser tab
- 👁️ **Live preview** of how links appear in the Contact section
- 🎨 **Custom icon/emoji** per link

### Social Link Fields:
| Field    | Description                          |
|----------|--------------------------------------|
| Platform | e.g., Facebook, LinkedIn, WhatsApp   |
| Label    | Display label (e.g., "Official Page") |
| URL      | Full link URL                        |
| Icon     | Emoji icon for the link              |

### Pre-configured Links (Sample):
| Platform     | Label         |
|--------------|---------------|
| 🔵 Facebook  | Official Page |
| 👤 Facebook  | CEO Profile   |
| 📍 Google Maps | Our Location |
| 💬 WhatsApp  | Contact Us    |

---

## Data Management

Central hub for all data operations.

### What you can do:
- 📊 **View data summary** — record counts for all modules
- 📥 **Export individual CSVs** per module:
  - Clients CSV
  - Applications CSV
  - Cases CSV
  - Appointments CSV
  - Services CSV
- 💾 **Export ALL data** in one full backup CSV file
- 📂 **Import individual CSVs** per module to restore specific data
- 🔄 **Reload sample data** — resets to built-in demo records
- 🗑️ **Clear all data** — permanently deletes all records
  (confirmation prompt required)

---

## Backup & Recovery

Protect your consultancy data with easy backup and restore tools.

### What you can do:
- 💾 **Download full backup** — exports all modules into one structured CSV
- 📂 **Restore from CSV**:
  - Click to browse for a CSV file
  - **Drag & drop** a CSV file onto the upload zone
- 🖼️ **Upload company logo** — replaces the default EC logo throughout the app
- ✅ **Status feedback** after import — shows number of records restored

### Backup CSV Structure:
```
### SECTION: CLIENTS ###
name,phone,email,type,status,...

### SECTION: APPLICATIONS ###
appNo,client,type,country,...

### SECTION: CASES ###
caseNo,client,title,...

... and so on
```

### Best Practices:
```
✅ Export a full backup before clearing data
✅ Store backups in OneDrive, Google Drive, or USB
✅ Use section-based full CSV for complete restores
✅ Use individual CSVs for targeted section restores
⚠️ localStorage is tied to the browser — always keep a CSV backup
```

---

## Settings & Customization

### 🎨 Appearance
- **Light Mode** — clean white professional theme
- **Dark Mode** — dark navy theme for low-light environments
- Toggle via the moon/sun icon in the topbar or from Settings
- **Compact Sidebar** — collapse to icon-only mode for more screen space

### 💬 WhatsApp Configuration
- Set the **official consultancy WhatsApp number**
- Number is used as the sender reference in all WhatsApp messages
- Format: `+92 300 0000000`

### 🔑 Password Management
- **Change your own password** — requires current password verification
- **Super Admin** can reset any user's password from the Users page

### 🖼️ Logo Upload
- Upload a custom company logo (PNG / JPG / GIF)
- Logo appears in the sidebar and login screen
- Saved in browser localStorage for the session

### ℹ️ About
- Application version
- Storage type
- Technology stack
- Developer credit (clickable → opens developer card popup)

---

## UI/UX Features

### 🎨 Design System
- **Modern SaaS dashboard** aesthetic
- Consistent card-based layout throughout
- Clean typography with proper hierarchy
- Red & Green brand color scheme
- Responsive grid layouts (4-col → 2-col → 1-col)

### ✨ Animations & Interactions
- Smooth **page transitions** with fade-in animation
- **Sidebar collapse** with smooth width transition
- **Hover effects** on cards, buttons, nav links, and table rows
- **Login orb animations** — floating ambient background
- **Toast notifications** — slide in/out from bottom-right
- **Modal animations** — slide up with backdrop blur
- Scrollbar styled to match brand colors

### 📱 Responsive Design
- **Desktop** — full sidebar + content layout
- **Tablet** — collapsible sidebar with overlay
- **Mobile** — hamburger menu, stacked grids, touch-friendly buttons
- Adaptive stat cards (4 → 2 → 1 column)
- Adaptive form grids (2-col → 1-col on small screens)

### 🔔 Toast Notifications
| Type    | Icon | When Used                        |
|---------|------|----------------------------------|
| Success | ✅   | Save, add, update, import        |
| Error   | ❌   | Failed login, validation errors  |
| Warning | ⚠️   | Delete confirmation, empty export |
| Info    | ℹ️   | Logout, informational messages   |

### 🔍 Search & Filter
- Real-time search on **every data table**
- Searches across **all fields** simultaneously
- Record count updates dynamically
- Empty state illustration when no results found

### 👨‍💻 Developer Card Popup
Clicking **"Developer Info"** in the footer opens a stylish popup card:
- Developer name and title
- Location badge
- Clickable links with icons:
  - 💬 WhatsApp
  - 🌐 Portfolio
  - 💼 LinkedIn
  - 📧 Email

---

## Developer Information

| Field      | Detail                                                        |
|------------|---------------------------------------------------------------|
| Name       | **Humam Khalil**                                              |
| Role       | Full-Stack Web Developer                                      |
| Location   | 📍 Peshawar, Pakistan                                         |
| WhatsApp   | [+92 302 849 2763](https://wa.me/923028492763)                |
| Portfolio  | [humamkhalil.netlify.app](https://humamkhalil.netlify.app)    |
| LinkedIn   | [Humam Khalil](https://linkedin.com/in/humam-khalil-1122b0344)|
| Email      | [humamkhalil11@gmail.com](mailto:humamkhalil11@gmail.com)     |

---

## Technical Notes

### Storage
```
Type:       Browser localStorage
Format:     JSON (automatic) + CSV (manual export)
Key:        ednex_v2_db
Session:    ednex_v2_session
Theme:      ednex_v2_theme
Logo:       ednex_v2_logo
```

### Data Modules
```
clients           → Client records
applications      → Visa/permit/admission applications
cases             → Legal and consultancy cases
appointments      → Scheduled appointments
services          → Service catalogue
religiousBookings → Hajj/Umrah/ticket bookings
educationApps     → Foreign education applications
socialLinks       → Dynamic social/contact links
countries         → Countries with universities
users             → System users (in-memory + localStorage)
msgLog            → WhatsApp message history (last 50)
```

### Browser Compatibility
| Browser       | Support |
|---------------|---------|
| Chrome 90+    | ✅ Full  |
| Edge 90+      | ✅ Full  |
| Firefox 88+   | ✅ Full  |
| Safari 14+    | ✅ Full  |
| Opera 76+     | ✅ Full  |
| IE 11         | ❌ Not supported |

### File Size
```
Single .html file — All HTML + CSS + JS combined
No external libraries, CDNs, or frameworks
No internet required for core functionality
```

---

## Keyboard Shortcuts

| Shortcut | Action                          |
|----------|---------------------------------|
| `Escape` | Close open modal or dialog      |
| `Enter`  | Submit login form               |

---

## Limitations & Notes

```
⚠️  Data is stored in the browser's localStorage.
    Clearing browser data / cache will erase all records.
    Always export a CSV backup regularly.

⚠️  localStorage is browser-specific.
    Data saved in Chrome will NOT appear in Firefox.

⚠️  WhatsApp messaging uses wa.me links (no official API key needed).
    It opens WhatsApp Web or the mobile app — the admin
    must click Send manually after the message pre-fills.

⚠️  Logo uploads are stored as base64 in localStorage.
    Very large images may slow down the page slightly.

⚠️  Passwords are stored in plain text (localStorage).
    This is suitable for internal/offline use only.
    For production deployment, use a proper backend.

✅  No installation required.
✅  No internet required for core features.
✅  No external libraries or CDNs.
✅  Works completely offline.
✅  All data exportable as standard CSV.
```

---

## Company Information

```
Company:   Ednex Consultant (Peshawar)
CEO:       Asfandyar Rabbani Advocate
Location:  Peshawar, Khyber Pakhtunkhwa, Pakistan
Facebook:  https://www.facebook.com/profile.php?id=61567980281187
CEO FB:    https://www.facebook.com/profile.php?id=61587981880912
Maps:      https://maps.app.goo.gl/Lz4hWf4DJrVPAaKw7
WhatsApp:  https://wa.me/923028492763
```

---

*© 2025 Ednex Consultant (Peshawar). All rights reserved.*
*Developed by [Humam Khalil](https://humamkhalil.netlify.app) · Peshawar, Pakistan*
```

---

Here is your complete **Markdown documentation file**. Save it as `README.md` or `FEATURES.md`. Here's a quick summary of what's covered:

| Section | What's Documented |
|---|---|
| 📋 **Overview** | What the app is, tech stack, file type |
| 🔐 **Auth & RBAC** | Credentials table, permissions matrix per role |
| 🏠 **Dashboard** | Stats, greetings, quick actions, recent clients |
| 👥 **Clients** | All CRUD fields, search, WhatsApp quick-send |
| 📄 **Applications** | Priority university selection, status tracking |
| ⚖️ **Cases** | Full case lifecycle management |
| 📅 **Appointments** | Scheduling and status tracking |
| 💬 **WhatsApp** | Templates, sending flow, message log |
| 🎓 **Foreign Education** | Countries, universities, priority selection |
| 🕌 **Religious Services** | Hajj, Umrah, Tickets, Ziyarat categories |
| 📋 **Services** | Catalogue management |
| 👤 **Users** | Super Admin RBAC, password reset |
| 🔗 **Social Links** | Dynamic management + preview |
| 🗃️ **Data/Backup** | CSV export/import, drag & drop restore |
| ⚙️ **Settings** | Theme, logo, WhatsApp config |
| 💻 **Technical** | Storage keys, browser support, limitations |
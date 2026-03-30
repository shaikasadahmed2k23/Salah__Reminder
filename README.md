# 🕌 Salah Reminder — Never Miss a Prayer

A comprehensive automated prayer reminder system that helps Muslims never miss their daily Salah (Islamic prayers). The system combines real-time prayer time tracking, automated Telegram notifications, and user engagement features to ensure prayers are performed on time.

## ✨ Features

### 🌍 Daily Prayer Times
- Automatically fetches daily prayer times at 12:01 AM using the **Aladhan API**
- Covers all five daily prayers: Fajr (🌙), Dhuhr (☀️), Asr (🌤️), Maghrib (🌇), and Isha (🌃)
- Location-based calculations (configurable city and country)
- Supports multiple Islamic calculation methods

### 🔔 Smart Prayer Calls
- Automated system checks every minute for upcoming prayer times
- Triggers reminder calls 15 minutes before each prayer (configurable offset)
- Seamless integration with Telegram for instant notifications
- Respects user time zones (currently set to IST/UTC+5:30)

### ✅ Telegram Check-In System
- Sends interactive Telegram messages 20 minutes after each prayer time
- Users confirm prayer completion through inline buttons
- Tracks prayer patterns and engagement
- Provides accountability through real-time check-ins

### 📊 Missed Prayer Tracking
- Monitors which prayers users have missed
- Sends reminders for uncompleted prayers
- Interactive buttons for confirming prayer completion
- Stores prayer status data for personal statistics

### 🔇 Do Not Disturb Mode
- Allows users to manage when they receive notifications
- Customizable prayer call preferences
- Respects user availability and preferences

## 🛠️ Tech Stack

- **Frontend**: HTML5 + CSS3 (responsive design with Islamic aesthetic)
- **Backend Automation**: n8n workflows
- **Database**: Supabase
- **Notifications**: Telegram Bot API
- **Prayer Data**: Aladhan API
- **Authentication**: Admin login for settings management

## 📁 Project Structure

```
├── index.html                    # Main user interface
├── admin.html                    # Admin dashboard for settings
├── Workflow 1 - Daily Prayer Times.json      # Fetches prayer times daily
├── Workflow 2 - Prayer Calls.json            # Triggers prayer reminders
├── Workflow 3 - Telegram Check-in.json       # Post-prayer confirmation
├── Workflow 4 - Missed Salah Reminder.json   # Tracks missed prayers
├── Workflow 5 - Don't Call Me.json           # Manages user preferences
└── workflow Images/              # Visual assets for workflows
```

## 🚀 How It Works

### Daily Flow:
1. **12:01 AM** - Workflow 1 fetches prayer times for the day from Aladhan API
2. **Every Minute** - Workflow 2 checks if it's time for a prayer call (15 min before prayer time)
3. **Prayer Time ± 20 min** - Telegram messages sent confirming prayer time
4. **20 Min After Prayer** - Workflow 3 sends check-in message asking "Did you pray?"
5. **User Response** - Workflow 4 processes button responses and updates prayer status
6. **User Preferences** - Workflow 5 allows users to disable/modify notifications

## 📱 User Interface

- **Beautiful Design**: Islamic-inspired color scheme with gold and green accents
- **Responsive**: Works seamlessly on mobile and desktop
- **Accessible**: Admin panel for managing prayer times and settings
- **Telegram Integration**: All notifications delivered through Telegram bot

## ⚙️ Configuration

The system uses Supabase as the database to store:
- Daily prayer times (Fajr, Dhuhr, Asr, Maghrib, Isha)
- User preferences and settings
- Prayer completion status
- Notification offset preferences (default: 15 minutes before prayer)

## 📌 Location Settings

Currently configured for:
- **City**: Kurnool, India
- **Country**: IN
- **Time Zone**: IST (UTC+5:30)
- **Calculation Method**: Karachi Method (Method 1)
- **School of Thought**: Hanafi (School 1)

*(These can be updated in Workflow 1 and associated settings)*

## 🔐 Security

- Admin panel with authentication
- Secure Supabase credentials management
- Telegram webhook for secure bot communications

---

*May Allah (SWT) accept our efforts and help us maintain our prayers on time. Ameen. 🤲*

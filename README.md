# Shift CSV → ICS Calendar Converter

A modern, user-friendly web application that converts shift schedule CSV files into ICS calendar format with timezone support and customizable reminders.

## 📋 Overview

This application is built using HTML, CSS, and Vanilla JavaScript to provide a seamless experience for converting work shift schedules into calendar events. The generated ICS files are compatible with all major calendar applications including Google Calendar, Outlook, Apple Calendar, and more.

## ✨ Features

- **CSV to ICS Conversion**: Convert shift schedules directly to calendar format
- **Timezone Support**: Handle multiple timezones including Estonia, Germany, UK, USA, Philippines, Singapore, India, Japan, and Australia
- **Customizable Events**: Edit event titles, locations, and notes
- **Smart Reminders**: Set custom reminder times (hours or minutes before events)
- **Schedule Analytics**: View weekly and monthly work hour summaries
- **Filter by Employee**: Preview and download schedules for specific team members
- **Cross-Platform**: Works in any modern web browser

## 🚀 Quick Start

1. **Download the Application**
   - Download `csv_parser.html` to your computer
   - Open the file in any modern web browser

2. **Prepare Your CSV File**
   - Ensure your CSV follows the required format (see Rules section below)
   - Name your file with month and year: `*_<Year>_<Month>_.csv`

3. **Convert Your Schedule**
   - Upload your CSV file
   - Configure timezone and reminder settings
   - Click "Parse & Preview" to review your events
   - Download the ICS file for your calendar

## 📁 File Format Requirements

### CSV File Rules

1. **File Extension**: Must be `.csv`
2. **Filename Format**: Must contain month and year as `*_<Year>_<Month>_.csv`
   - ✅ Valid: `schedule_2025_01.csv`, `shifts_2025_12.csv`
   - ❌ Invalid: `schedule.csv`, `january2025.csv`

3. **CSV Structure**: Your CSV must follow this exact format:

```csv
Name,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31
John Doe,09:00,09:00,OFF,09:00,09:00,OFF,OFF,09:00,09:00,09:00,OFF,09:00,09:00,OFF,OFF,09:00,09:00,09:00,OFF,09:00,09:00,OFF,OFF,09:00,09:00,09:00,OFF,09:00,09:00,OFF,OFF
,17:00,17:00,,17:00,17:00,,,,17:00,17:00,17:00,,17:00,17:00,,,,17:00,17:00,17:00,,17:00,17:00,,,,17:00,17:00,17:00,,17:00,17:00,,,
Jane Smith,OFF,OFF,09:00,OFF,OFF,09:00,09:00,OFF,OFF,OFF,09:00,OFF,OFF,09:00,09:00,OFF,OFF,OFF,09:00,OFF,OFF,09:00,09:00,OFF,OFF,OFF,09:00,OFF,OFF,09:00,09:00
,,,17:00,,,17:00,17:00,,,,17:00,,,17:00,17:00,,,,17:00,,,17:00,17:00,,,,17:00,,,17:00,17:00
```

**Key Points:**
- First row: Column headers with "Name" and day numbers (1-31)
- Even rows: Employee names and start times (HH:MM format)
- Odd rows: Corresponding end times (leave empty for OFF days)
- Use "OFF" or "vac" for days off
- Time format: 24-hour format (e.g., 09:00, 17:00)

## 🖼️ Screenshots

*Add your application screenshots here*

### Main Interface
![Main Interface](screenshots/main-interface.png)
*Upload CSV file and configure settings*

### Preview and Analytics
![Preview and Analytics](screenshots/preview-analytics.png)
*Review events and view work hour analytics*

### Calendar Integration
![Calendar Integration](screenshots/calendar-integration.png)
*Imported events in Google Calendar*

## 📖 Detailed Usage Instructions

### Step 1: Upload Your CSV File
1. Click "Choose File" and select your schedule CSV
2. Ensure the filename contains the correct month and year format

### Step 2: Configure Settings
- **Event Title Template**: Customize how events appear in your calendar
  - `{name}` - Employee name
  - `{date}` - Event date (MM/DD/YYYY)
  - `{weekday}` - Day of the week (Mon, Tue, etc.)
- **Source Time Zone**: Select your local timezone
- **Reminder**: Set how far in advance you want to be reminded

### Step 3: Parse and Preview
1. Click "Parse & Preview" to process your CSV
2. Review the generated events in the preview table
3. Edit locations (Office/Home) and event notes as needed
4. Use the name filter to view specific employees

### Step 4: Download ICS File
1. Click "Download ICS" to generate your calendar file
2. The file will be named based on your selection (All employees or specific person)
3. Import the ICS file into your preferred calendar application

## 🗓️ Calendar Integration

### Google Calendar
1. Open Google Calendar
2. Click the "+" button and select "Import"
3. Choose your downloaded ICS file
4. Select which calendar to import to
5. Click "Import"

### Microsoft Outlook
1. Open Outlook
2. Go to File → Open & Export → Import/Export
3. Select "Import an iCalendar (.ics) or vCalendar file"
4. Choose your downloaded ICS file
5. Follow the import wizard

### Apple Calendar
1. Open Calendar app
2. Go to File → Import
3. Select your downloaded ICS file
4. Choose which calendar to import to
5. Click "Import"

## 🔧 Advanced Features

### Schedule Analytics
- View weekly work hour summaries
- Track total hours per employee
- See work vs. rest day distribution
- Filter analytics by specific employees

### Customization Options
- Edit event titles and descriptions
- Set different locations (Office/Home)
- Configure reminder times
- Filter events by employee name

### Timezone Handling
The application properly handles timezone conversions and daylight saving time changes for all supported regions.

## 🛠️ Technical Details

- **Built with**: HTML5, CSS3, Vanilla JavaScript
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **File Processing**: Client-side only (no data sent to servers)
- **ICS Standard**: RFC 5545 compliant
- **Timezone Database**: Uses browser's Intl.DateTimeFormat API

## 📝 Troubleshooting

### Common Issues

**"Could not detect year and month in filename"**
- Ensure your filename contains the format `*_<Year>_<Month>_.csv`
- Example: `schedule_2025_01.csv`

**"No 'Name' column found"**
- Make sure your CSV has a column header exactly named "Name"
- Check for typos or extra spaces

**Events not showing correct times**
- Verify your CSV uses 24-hour format (HH:MM)
- Check that start and end times are in the correct rows

**ICS file not importing**
- Ensure your calendar application supports ICS format
- Try importing a smaller subset of events first
- Check that the file isn't corrupted during download

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

## 📞 Support

For support or questions, please open an issue in the project repository.

---

**Made with ❤️ for efficient schedule management**
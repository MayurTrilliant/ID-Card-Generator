# Priyadarshani Form

React form for Priyadarshani High School CBSE Bhosari 2026-27.

## Google Sheets connection

Create a Google Apps Script web app for your sheet and set its deployment URL in `.env`:

```env
VITE_GOOGLE_SHEET_WEB_APP_URL=https://script.google.com/macros/s/YOUR_DEPLOYMENT_ID/exec
```

Use the code from `google-apps-script.gs` in Apps Script. It automatically creates the response sheet columns, saves each uploaded photo as a real Google Drive image, and stores a clickable `Download Photo` link in the sheet instead of base64 text.

Expected request body:

```json
{
  "studentName": "Student name",
  "classDiv": "Nursery - Angel",
  "birthdate": "19 Oct 2022",
  "address": "Address",
  "motherContact": "9834440493",
  "fatherContact": "8237377214",
  "photo": "base64 image data",
  "photoFileName": "Student-name-123456789.jpg",
  "submittedAt": "ISO timestamp"
}
```

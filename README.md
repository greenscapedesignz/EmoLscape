# 🌿 EmoL'scape - Greenscape Designz Happiness Index™
## Secure Mobile-Friendly Web Application

---

## 🎯 Features

### ✅ **Security & Access Control**
- **Registration Gate**: Users must provide Name, Email, and Mobile to access
- **Data Collection**: All registrations saved to Google Sheets automatically
- **Protected API**: Your Gemini API key is completely hidden from users
- **Rate Limiting**: 30 requests per minute to prevent abuse

### 📱 **Mobile Optimized**
- Fully responsive design for iOS and Android
- Touch-optimized sliders and buttons
- Native app-like experience
- Safe area insets for modern phones

### 🤖 **AI Features**
1. **EmoL Chatbot**
   - "Hello! I'm EmoL, your AI Landscape Consultant. How can I assist you today?"
   - Context-aware responses based on audit scores
   - Conversational interface

2. **Renovation Roadmap**
   - AI-generated improvement strategies
   - Focus on lowest-performing pillars
   - Actionable design interventions

3. **Biodiversity Plant List**
   - Location-specific native plants
   - Trees, Shrubs, and Groundcovers
   - Ecological benefits and maintenance info

4. **Auto Email Draft**
   - Professional client communication
   - Includes audit summary
   - Signature: Anirban Pal, Greenscape Designz

---

## 🚀 Quick Start

### 1. Install Dependencies

```bash
npm install
```

### 2. Set Up Google Sheets

#### Create Spreadsheet
1. Go to [Google Sheets](https://sheets.google.com)
2. Create new spreadsheet: **"EmOL'scape-Greenscape Designz Happiness Index"**
3. Create sheet: **"Registrations"**
4. Add headers: `Timestamp | Name | Email | Mobile | IP Address`
5. Copy Spreadsheet ID from URL

#### Create Service Account
1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Enable Google Sheets API
3. Create Service Account
4. Download JSON key
5. Share spreadsheet with service account email
6. Add credentials to `.env`

### 3. Configure Environment

Update `.env` file:
```env
GEMINI_API_KEY=AIzaSyAxZNYUPasJ5YR6EHyjuwG1OR3Wa97Ld7U
GOOGLE_SHEETS_ID=your_spreadsheet_id
GOOGLE_SERVICE_ACCOUNT={"type":"service_account",...}
```

### 4. Start Server

```bash
npm start
```

Visit: `http://localhost:3000`

---

## 📊 API Endpoints

### `POST /api/register`
Register new user, save to Google Sheets

### `POST /api/gemini`
AI consultation endpoint

### `GET /health`
Health check

---

## 🌐 Deployment

### Heroku
```bash
heroku create emolscape-gdhi
heroku config:set GEMINI_API_KEY=your_key
heroku config:set GOOGLE_SHEETS_ID=your_id
heroku config:set GOOGLE_SERVICE_ACCOUNT='{"type":...}'
git push heroku main
```

### Vercel
```bash
vercel
# Add environment variables in dashboard
```

---

## 🔧 Customization

**Change AI Model** (server.js line 26):
```javascript
const GEMINI_MODEL = "gemini-2.0-flash-exp";
```

**Update Signature** (public/index.html):
```javascript
Sincerely,
Anirban Pal
Landscape Architect
anirban.pal@greenscapedesignz.in
+91 88613 17426
```

---

## 🐛 Troubleshooting

**Registration Failed:**
- Check Google Sheets ID
- Verify service account has Editor access
- Ensure "Registrations" sheet exists

**API Errors:**
- Verify `GEMINI_API_KEY` in `.env`
- Restart server after changes
- Check rate limits

---

## 📱 User Flow

1. **Registration** → Name, Email, Mobile
2. **Dashboard** → Project details + 8 GDHI pillars
3. **AI Tools** → Chat, Roadmap, Plants, Email
4. **Certificate** → Professional PDF output

---

## 🔒 Security

✅ API key never exposed to frontend  
✅ Input validation and sanitization  
✅ Rate limiting enabled  
✅ HTTPS recommended for production  

---

## 📈 Data Collection

All registrations auto-saved to Google Sheets:

| Timestamp | Name | Email | Mobile | IP Address |
|-----------|------|-------|--------|------------|
| 2024-01-15T10:30:00Z | John Doe | john@example.com | 9876543210 | 192.168.1.1 |

---

## 🤝 Support

**Contact:**
- Email: anirban.pal@greenscapedesignz.in
- Phone: +91 88613 17426

---

**Built with ❤️ by Greenscape Designz**

🔒 Secure | 📱 Mobile-First | 🤖 AI-Powered

# 🎯 Vantage Tools

Web interfaces for automation workflows. Simple, bookmark-able tools that connect to n8n webhooks for instant results.

## 🚀 Live Tools

### 📝 [Script Generator](https://realmreynolds.github.io/vantage-tools/script-generator.html)
Generate professional scripts with custom length, tone, and context. Perfect for client presentations, social media, or internal communications.

**Status:** ✅ Live  
**Deadline:** Testing by Thanksgiving

### 📰 [Defense Dispatch Curation](https://realmreynolds.github.io/vantage-tools/defense-dispatch.html)
Visual story curation interface for daily news readouts. Alternative to Google Sheets with cleaner UX.

**Status:** 🚧 In Development  
**Deadline:** Monday

### 📋 [Brief Request Form](https://realmreynolds.github.io/vantage-tools/brief-request.html)
Request custom research briefs from the team with automatic routing and notifications.

**Status:** 📅 Coming Soon  
**Deadline:** Testing by Thanksgiving

## 🏗️ Architecture

```
User fills form → GitHub Pages (static HTML)
                       ↓
                  POST to webhook
                       ↓
              n8n workflow processes
                       ↓
              Results display on page
```

**Tech Stack:**
- Frontend: Vanilla HTML/CSS/JavaScript
- Hosting: GitHub Pages (free)
- Backend: n8n workflows
- No authentication required

## 📂 Repository Structure

```
vantage-tools/
├── index.html              # Dashboard landing page
├── script-generator.html   # Script generation tool
├── defense-dispatch.html   # News curation interface
├── brief-request.html      # Brief request form
└── README.md              # This file
```

## 🔧 Setup Instructions

### For End Users
1. Bookmark: `https://realmreynolds.github.io/vantage-tools/`
2. Click on any tool
3. Fill out the form
4. Get instant results

### For Developers

**Prerequisites:**
- n8n instance with webhook endpoints
- GitHub account

**Configuration:**
Each HTML file has a `CONFIG` object at the top of the `<script>` section:

```javascript
const CONFIG = {
    webhookUrl: 'https://your-n8n-instance.app.n8n.cloud/webhook/endpoint',
    timeout: 60000
};
```

Update `webhookUrl` with your actual n8n webhook endpoint.

**n8n Workflow Requirements:**
- Must accept POST requests with JSON body
- Must return JSON response
- Response format varies by tool (see individual tool docs)

## 🎨 Design Philosophy

- **Simple:** No login, no complex navigation
- **Fast:** Pure HTML/CSS/JS, no frameworks
- **Mobile-friendly:** Responsive design works everywhere
- **Professional:** Clean UI with modern branding
- **Reliable:** Clear feedback, error handling, loading states

## 📱 Mobile Support

All tools are fully responsive and work on:
- Desktop browsers
- Tablets
- Mobile phones

## 🔐 Security Notes

- No user authentication required
- No sensitive data stored in frontend
- All processing happens in secure n8n workflows
- Webhook URLs should be kept private

## 🚀 Deployment

This repo uses GitHub Pages for automatic deployment:

1. Push changes to `main` branch
2. GitHub Pages rebuilds site (1-2 minutes)
3. Changes go live at `https://realmreynolds.github.io/vantage-tools/`

## 📊 Usage Stats

Track usage by adding UTM parameters to webhook calls and monitoring n8n execution logs.

## 🤝 Contributing

For questions or feature requests, contact the project maintainer.

## 📝 License

Internal use only

---

**Built with ❤️ by the team**  
Powered by [n8n automation](https://n8n.io)

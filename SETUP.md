# Vantage Tools - Setup Checklist

## Step 1: Create GitHub Repository ✓

1. Go to https://github.com/new
2. Repository name: `vantage-tools`
3. Description: "Web interfaces for Vantage automation workflows"
4. Set to **Public**
5. ✅ Check "Add a README file"
6. Click "Create repository"

## Step 2: Enable GitHub Pages

1. In your new repo, click **Settings**
2. Scroll to **Pages** in left sidebar
3. Under "Source", select **Deploy from a branch**
4. Branch: **main** / (root)
5. Click **Save**
6. Wait 1-2 minutes for deployment

## Step 3: Upload Files

Upload these 4 files to your repo:

- [ ] `index.html` (Dashboard)
- [ ] `script-generator.html` (Script tool)
- [ ] `README.md` (Documentation)
- [ ] `SETUP.md` (This file - optional)

**How to upload:**
1. Click "Add file" → "Upload files"
2. Drag all files at once
3. Commit message: "Initial commit - Vantage Tools dashboard and script generator"
4. Click "Commit changes"

## Step 4: Configure Webhook URLs

For **script-generator.html**, update line 371:

```javascript
webhookUrl: 'https://targeted-victory.app.n8n.cloud/webhook/script-generator'
```

Replace with your actual n8n webhook URL.

## Step 5: Test It!

1. Wait 2-3 minutes after uploading
2. Visit: `https://realmreynolds.github.io/vantage-tools/`
3. Click "Script Generator"
4. Fill out form and test submission

## Step 6: Bookmark & Share

Your team URLs:
```
Dashboard: https://realmreynolds.github.io/vantage-tools/
Script Generator: https://realmreynolds.github.io/vantage-tools/script-generator.html
```

## Next Steps

- [ ] Build Defense Dispatch interface (Priority: Monday)
- [ ] Build Brief Request form (Priority: Thanksgiving)
- [ ] Add more tools as needed
- [ ] Update dashboard with new tools

## Troubleshooting

**404 Error?**
- Wait 2-3 minutes after uploading
- Check GitHub Pages is enabled in Settings
- Verify files are in root directory (not in a subfolder)

**Webhook not working?**
- Check webhook URL in script
- Verify n8n workflow is Active
- Test webhook directly with curl/Postman
- Check browser console for errors (F12)

**Styling looks broken?**
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache
- Try incognito/private browsing mode

## Files Location

All files are in `/home/claude/` in this Claude conversation:
- `/home/claude/index.html`
- `/home/claude/script-generator.html`
- `/home/claude/README.md`
- `/home/claude/SETUP.md` (this file)

Download them and upload to GitHub!

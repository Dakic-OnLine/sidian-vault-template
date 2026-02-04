# Setup Guide

Complete guide to setting up your Sidian Vault as a personal productivity system.

---

## Step 1: Make This Vault Your Own

This template is connected to a GitHub repository. To make it truly yours, you have two options:

### Clone and Detach

1. **Clone or download this vault**
   ```bash
   git clone https://github.com/your-username/sidian-vault.git
   cd sidian-vault
   ```

2. **Remove the git history** (makes it a fresh vault)
   ```bash
   rm -rf .git
   ```

3. **Initialize as your own repository** (optional)
   ```bash
   git init
   git add .
   git commit -m "Initial commit - my personal vault"
   ```

4. **Connect to your own GitHub** (optional)
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```

---

## Step 2: Install Obsidian

1. **Download Obsidian** from [obsidian.md](https://obsidian.md)
2. Install it on your devices:
   - **Desktop**: Download for Windows, Mac, or Linux
   - **Mobile**: Get Obsidian app from App Store or Google Play

---

## Step 3: Open Your Vault

### On Desktop

1. Open Obsidian
2. Click **"Open folder as vault"**
3. Navigate to and select the `sidian-vault` folder
4. Click **"Open"**

### On Mobile

1. Open Obsidian app
2. Tap **"Create new vault"** or **"Open folder as vault"**
3. Navigate to your vault location:
   - **iOS**: Files app → On My iPhone/iPad → your vault folder
   - **Android**: File manager → your vault folder
4. Tap to open

---

## Step 4: Configure Obsidian Settings

### Essential Settings

1. **Open Settings** (gear icon, bottom left)

2. **File & Link Links**
   - ✅ **Detect all links**
   - ✅ **Automatically update internal links**

3. **Editor**
   - **Spellcheck**: Enable for your language
   - **Line numbers**: Show or hide as preferred

4. **Appearance**
   - **Base mode**: Light or Dark
   - Choose a theme you like (Default themes work well)

5. **Daily Notes** (optional, for quick access)
   - Set template file location if you want hotkey access
   - New file location: `02_Diary`
   - Date format: `YYYY-MM-DD`

---

## Step 5: Enable Core Plugins

1. Go to **Settings** → **Core Plugins**
2. Enable these plugins:
   - ✅ **Daily notes** (if you want quick diary creation)
   - ✅ **Templates** (to use templates from `99_Assets/templates/`)
   - ✅ **Graph view** (to see connections between notes)
   - ✅ **Backlinks** (shows which notes link to current note)
   - ✅ **Outgoing links** (shows links from current note)

### Configure Templates Plugin

1. Go to **Settings** → **Templates**
2. **Template folder location**: `99_Assets/templates`
3. **Daily note template**: `99_Assets/templates/tm_daily.md`
4. **Use date format**: `YYYY-MM-DD`

---

## Step 6: Install Recommended Plugins (Optional)

### Obsidian Git (for backup)

1. Go to **Settings** → **Community Plugins**
2. Turn on **Restricted mode** (allows third-party plugins)
3. Click **Browse** and search for "Obsidian Git"
4. Install and enable

**Configure Obsidian Git:**
1. Go to **Settings** → **Obsidian Git**
2. Set **Git dir** to `.` (current directory)
3. Set **Auto-commit interval** (e.g., every 30 minutes)
4. Set **Auto-push interval** (e.g., every 60 minutes)

### Dataview (for advanced queries)

1. Search for "Dataview" in community plugins
2. Install and enable
3. Use for querying your goals, diary entries, etc.

---

## Step 7: Personalize Your Vault

### Edit Home.md

1. Open `Home.md`
2. Replace sample content with your own:
   - Your current goals
   - Your recent activity
   - Your focus areas

### Update Your First Goal

1. Open `03_Goals/Example - Learn Spanish.md`
2. Use it as a template, or delete and create your own goal
3. Remember to add properties at the top:
   ```yaml
   ---
   status: active
   area: learning
   target_date: YYYY-MM-DD
   priority: high
   ---
   ```

### Create Your First Diary Entry

1. Navigate to `02_Diary/`
2. Create a new file named with today's date: `YYYY-MM-DD.md`
3. Use the template from `99_Assets/templates/tm_daily.md`
4. Write about your day

---

## Step 8: Set Up Sync Across Devices

### Option A: Obsidian Sync (Official, Paid)

1. Create an Obsidian account
2. Go to **Settings** → **Sync**
3. Purchase sync subscription
4. Enable sync on all devices
5. Your vault stays in sync automatically

### Option B: Git + GitHub (Free, Technical)

1. Create a private GitHub repository
2. Push your vault to GitHub
3. Use Obsidian Git plugin to auto-commit and push
4. Pull changes on other devices

### Option C: Cloud Storage (Dropbox, OneDrive, etc.)

1. Move your vault folder to your cloud storage folder
2. Install the cloud service on all devices
3. Open the synced folder in Obsidian on each device

**Note**: Be careful with sync conflicts. Consider using sync for one device type and Git for backup.

---

## Step 9: Start Using the System

### Daily Workflow

1. **Morning** - Open `Home.md` to see your focus
2. **Capture** - Use `Inbox.md` for quick thoughts throughout the day
3. **Journal** - End day by writing in `02_Diary/YYYY-MM-DD.md`
4. **Review** - Check off completed tasks in goal plans

### Weekly Workflow

1. Create a new weekly plan in `30_Weekly_Plans/YYYY-W##.md`
2. Review past week's diary entries
3. Set 1-2 main focuses
4. Break down into daily tasks

### Monthly Workflow

1. Create monthly review in `31_Monthly_Reviews/YYYY-MM.md`
2. Review all active goals
3. Adjust priorities based on progress
4. Plan next month's focus

---

## Step 10: Customizing the System

### Add Your Own Templates

1. Go to `99_Assets/templates/`
2. Create new template files with `tm_` prefix
3. Access them from the Templates plugin

### Modify Folder Structure

The numbered folders are organized by purpose:

| Prefix | Purpose |
|--------|---------|
| `01_` | Input (thinking, ideas) |
| `02_` | Daily (journaling) |
| `03_` | Goals & tracking |
| `30_` | Weekly planning |
| `31_` | Monthly reviews |
| `32_` | Quarterly strategy |
| `50_` | Output (reports) |
| `92_` | Longer content |
| `99_` | Resources (templates) |

Feel free to add folders within this system as needed.

---

## Troubleshooting

### "Workspace file changes" warning

This is normal if you use multiple devices. The `.obsidian/workspace` file tracks your open files. It's excluded from git by default.

### Plugins not syncing

- Community plugins need to be installed on each device separately
- Plugin settings sync if your vault syncs, but the plugin itself doesn't

### Can't see properties panel

- Make sure you're on Obsidian version 1.4+ (properties are built-in)
- Click the "Add property" button at the top of any file

### Git conflicts

- If you get merge conflicts, don't panic
- Your content files are rarely affected
- Usually just `.obsidian/workspace` or plugin data
- Resolve by keeping your local changes

---

## Next Steps

1. ✅ Make this vault your own (detach from template repo)
2. ✅ Set up Obsidian on your devices
3. ✅ Create your first goal and diary entry
4. ✅ Explore the template files to understand the system
5. ✅ Read `Guide.md` for detailed system documentation
6. ✅ Check `Guide - Tag System.md` and `Guide - Properties.md` for advanced usage

---

## Need Help?

- **Documentation**: See `Guide.md` for complete system reference
- **Community**: [Obsidian Forum](https://forum.obsidian.md/)
- **Discord**: [Obsidian Discord Server](https://discord.gg/veHUWu6kTn)

---

**Enjoy your Sidian Vault!**

This system is designed to grow with you. Start simple, add complexity as you become comfortable.

# PageMotor Local Setup for Mac

A one-click Mac app that installs everything you need to run PageMotor locally.

## What It Installs

- **Homebrew** (Mac package manager)
- **PHP 8.4** (the language PageMotor runs on)
- **MySQL** (database for your pages, users, and settings)
- **Mailpit** (catches emails locally so nothing gets sent to real inboxes)
- **Node.js** (required by Claude Code)
- **GitHub CLI** (push code and manage repos from the command line)
- **VS Code** (free code editor)
- **Claude Code** (AI assistant that lives inside VS Code)

## How to Use

### 1. Download

**[Download PageMotor Local Setup](../../releases/latest/download/PageMotor-Local-Setup.zip)**

### 2. Unzip

Double-click the `.zip` file. You'll get a `PageMotor Local Setup.app` file.

### 3. Open It (Read This Part Carefully)

Your Mac will try to block this app because it wasn't downloaded from the App Store. This is normal and expected. Here's how to get past it:

1. **Double-click** the app. You'll see a scary warning saying Apple can't verify it. **Click Done.** (Do NOT click "Move to Bin.")
2. Open **System Settings** (click the Apple menu in the top-left corner of your screen, then System Settings).
3. Click **Privacy & Security** in the left sidebar.
4. Scroll down. You'll see a message that says something like: *"PageMotor Local Setup.app" was blocked from use because it is not from an identified developer.*
5. Click **Open Anyway**.
6. Your Mac will ask for your password. Enter it.
7. You'll see one more warning. Click **Open**.

This only happens the first time. After that, the app opens normally.

### 4. Follow the Steps

The app walks you through everything with simple dialog boxes. Each step has a **Skip** and **Continue** button so you're always in control.

Here's what to expect:

| Step | What Happens | Time |
|------|-------------|------|
| 1 | Installs Homebrew | 2-5 min |
| 2 | Installs PHP | 1-2 min |
| 3 | Installs MySQL, asks you to pick a password | 1-2 min |
| 4 | Installs Mailpit, configures PHP to use it | 1 min |
| 5 | Installs Node.js | 1 min |
| 6 | Installs GitHub CLI, asks for your name/email, logs you into GitHub | 2-3 min |
| 7 | Installs VS Code | 1-2 min |
| 8 | Installs Claude Code extension | 30 sec |
| 9 | Sets up your PageMotor project folder | 1 min |

Total: about 15-20 minutes, mostly waiting for downloads.

### 5. You're Done

When it finishes, you'll see a cheat sheet:

| What | Where |
|------|-------|
| Your site | http://localhost:8000 |
| Admin panel | http://localhost:8000/admin/ |
| Email inbox | http://localhost:8025 |
| Claude Code | Sidebar icon in VS Code |

## Starting PageMotor After a Restart

MySQL and Mailpit start automatically when your Mac boots. But the PageMotor server needs to be started manually.

Open Terminal and run:

```
cd ~/path/to/your/pagemotor/folder
php -S localhost:8000
```

Leave that Terminal window open while you work. Close it (or press `Ctrl+C`) to stop the server.

## Requirements

- macOS 13 (Ventura) or later
- An internet connection (for downloading packages)
- A free GitHub account (sign up at github.com)
- A Claude account at claude.ai (Pro subscription includes Claude Code)

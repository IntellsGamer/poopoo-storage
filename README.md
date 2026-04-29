
# 💩 poopoo-storage
[![Poo poo Downloader](https://img.shields.io/badge/Poo%20poo-Downloader-orange?style=flat-square)](https://github.com/IntellsGamer/poopoo-storage)
[![GitHub last commit](https://img.shields.io/github/last-commit/IntellsGamer/poopoo-storage?style=flat-square)](https://github.com/IntellsGamer/poopoo-storage/commits/main)
[![Repo Size](https://img.shields.io/github/repo-size/your-username/poopoo-storage?style=flat-square)](https://github.com/IntellsGamer/poopoo-storage)

> **⚠️ WARNING: This repository is automatically managed by the Poo poo Downloader Action**  
> Do not manually edit files in the `downloads/` folder. Changes will be overwritten.

---

## 📦 What is this?

This is a **dedicated storage repository** for all content downloaded by the [Poo poo Downloader](https://github.com/IntellsGamer/poopoo-saver) GitHub Action.

All YouTube videos, playlists, and other files are stored here to keep the main repository clean and lightweight.

---

## 📁 Repository Structure

```

poopoo-storage/
├── downloads/              # All downloaded content
│   ├── video_id.mp4       # Single videos
│   ├── playlist_name/     # Playlist subfolders (if folder mode)
│   │   ├── 01_title.mp4
│   │   ├── 02_title.mp4
│   │   └── ...
│   └── archive_*.zip      # Zip archives (if zip mode enabled)
└── README.md              # This file

```

---

## 🎯 File Naming Convention

Files are named using customizable patterns. Default pattern: `{date}_{id}.ext`

| Placeholder | Description | Example |
|-------------|-------------|---------|
| `{date}` | Download date (YYYYMMDD_HHMMSS) | `20250115_143022` |
| `{id}` | YouTube video ID | `dQw4w9WgXcQ` |
| `{title}` | Video title (sanitized) | `Rick_Astley_Never_Gonna_Give` |
| `{index}` | Position in playlist | `01`, `02`, `03` |
| `{playlist_title}` | Playlist name | `My_Favorite_Songs` |

### Examples:
- `20250115_143022_dQw4w9WgXcQ.mp4` - Single video
- `01_Rick_Astley_Never_Gonna_Give.mp3` - Audio from playlist
- `My_Favorite_Songs/03_2000s_mix.mkv` - Playlist folder mode

---

## 🎬 Supported Content Types

- ✅ YouTube videos (any quality)
- ✅ YouTube playlists (full or selective)
- ✅ YouTube Shorts
- ✅ Direct file URLs (MP4, MP3, ZIP, etc.)
- ✅ Age-restricted content (via Cloudflare WARP)
- ✅ Geo-blocked content (via Cloudflare WARP)

---

## 🔄 Auto-Generated Content

All content in `downloads/` is **automatically**:

1. Downloaded via GitHub Actions
2. Converted to requested format (MP4, MP3, MKV, WEBM, etc.)
3. Split into parts if exceeding size threshold
4. Committed and pushed to this repository
5. Organized by playlist folders (if enabled)

**Do not manually add, modify, or delete files** in the `downloads/` folder unless you know what you're doing.

---

## 📊 Repository Statistics

This repository is designed to handle:

| Metric | Limit |
|--------|-------|
| Individual file size | Unlimited (auto-split >90MB) |
| Total repository size | GitHub's soft limit: 100GB (contact support for more) |
| Recommended max | 50GB for optimal performance |
| File count | Unlimited (thousands of files) |

> 💡 **Tip**: Use the cleanup workflow periodically to remove old files and keep the repo size manageable.

---

## 🧹 Cleanup Instructions

### Option 1: Using GitHub Action (Recommended)

1. Go to **Actions** tab → **"Poo poo - Clean poopoo-storage"**
2. Click **"Run workflow"**
3. Choose cleanup mode:
   - `all` - Delete everything
   - `older_than_30_days` - Delete old files only
   - `specific_folder` - Delete a specific playlist folder
4. Type `DELETE` to confirm
5. Run workflow

### Option 2: Manual Cleanup

```bash
# Clone the repository
git clone https://github.com/your-username/poopoo-storage.git
cd poopoo-storage

# Delete specific files/folders
rm -rf downloads/specific_file.mp4
rm -rf downloads/playlist_folder/

# Commit and push
git add .
git commit -m "Manual cleanup"
git push
```

Option 3: Permanent History Cleanup (⚠️ Destructive)

To remove files from git history completely:

```bash
# Install git-filter-repo
pip install git-filter-repo

# Remove downloads folder from history
git filter-repo --path downloads --invert-paths --force

# Force push
git push origin --force --all
```

⚠️ Warning: This rewrites history. All contributors must re-clone.

---

📋 Common Queries

Q: Why is my video missing?

A: Check the source repository's Actions logs. The download may have failed due to:

· Age restriction (should work with WARP)
· Deleted/private video
· YouTube region block
· Network timeout

Q: Can I download a video again?

A: Yes! Run the downloader workflow again. Files with the same name will be overwritten.

Q: How do I free up space?

A: Use the cleanup workflow or manually delete old files. Consider keeping only the last 30 days.

Q: Can I access these files directly?

A: Yes! Raw file URLs:
https://raw.githubusercontent.com/your-username/poopoo-storage/main/downloads/filename.mp4

---

🔗 Related Repositories

Repository Purpose
main-repo Source code and workflows
poopoo-storage (this repo) Downloaded content storage

---

📝 License

This repository contains downloaded content. Each file is subject to its original creator's copyright. Use responsibly.

The automation scripts are provided under MIT License.

---

🛟 Support

· Check the source repository's Actions tab for logs
· Review the Poo poo Downloader documentation
· Open an issue in the source repository

---

📊 Badges

https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
https://img.shields.io/badge/Maintained%3F-yes-blue.svg?style=flat-square
https://img.shields.io/github/license/your-username/poopoo-storage?style=flat-square

---

💩 poopoo-storage - Where downloaded content lives happily ever after.
Last updated: Automatically with each download

```

This README includes:

- ✅ Clear warning that it's auto-managed
- ✅ File structure explanation
- ✅ Naming convention guide
- ✅ Supported content types
- ✅ Cleanup instructions (multiple methods)
- ✅ FAQ section
- ✅ Badges for visual appeal
- ✅ Links back to source repository
